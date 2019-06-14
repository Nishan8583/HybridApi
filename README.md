# Go Package to communicate with Hybrid Analysis

## Installation
```go
  go get github.com/Nishan8583/HybridApi/Hybrid
```

## Example:
```go
package main;

import (
    "github.com/Nishan8583/HybridApi/Hybrid";
  "fmt";

)
func main() {
  h, err := Hybrid.HybridInit("<API-KEY>"); // The api key will be used
  if err != nil {
    fmt.Println("Could not Create Hybrid Type",err);
    return;
  }
  
  // Some of the lines are commented, but use it as shown below
  //resp,err := h.ReportSummary([]string{"603a72e1aad833b92a6ef7edac65849c3d899b4b7eaac399abf2f6d2cbb4b1e7","c7acf3c1167ae28439a22bec62e35303fd34043c600a6ad333cfe115a2b12e98"});
  //resp,err := h.OverviewSummary("c7acf3c1167ae28439a22bec62e35303fd34043c600a6ad333cfe115a2b12e98");
  //resp,err := h.SearchHash("c7acf3c1167ae28439a22bec62e35303fd34043c600a6ad333cfe115a2b12e98");
  //resp,err := h.SearchQuery("domain","google.com");
  //resp, err := h.AnalyzeFile("E:\\GoLang\\8_Hybrid_Analysis_Library\\src\\main.go",map[string]string{"environment_id":"300");
  //resp, err := h.AnalyzeURLFile("https://www.blackhat.com/presentations/bh-usa-04/bh-us-04-chambet/bh-us-04-chambet-google-up.pdf",map[string]string{"environment_id":"300"});
  //resp, err := h.AnalyzeURL("https://medium.com/@masnun/making-http-requests-in-golang-dd123379efe7",map[string]string{"environment_id":"300"});
  //resp, err := h.AnalyzeURLHash("https://www.blackhat.com/presentations/bh-usa-04/bh-us-04-chambet/bh-us-04-chambet-google-up.pdf");
  //resp, err := h.AnalyzeDroppedFiles("e5b9ce395b80a7b55af07915923cd282589c6c4c9f079efc25827dcf11e6b9ec","7cff31263aaf801db3d229b44f77658736188f18578dce4594d71c514c8e412f");
  //resp, err := h.ScanState();
  resp,err := h.ScanResultId("5cf8c662028838c232ebc6bb")

  if err != nil {
    fmt.Println(err);
  }
  fmt.Println(resp);
}
```

## INFO
Some api have not been implemented yet, since I did not see many people using them
