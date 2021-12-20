<!-- start title -->
<!-- end title -->
<!-- start description -->
<!-- end description -->
<!-- start contents -->
<!-- end contents -->
<!-- start usage -->
<!-- end usage -->
<!-- start inputs -->
<!-- end inputs -->
<!-- start outputs -->
<!-- end outputs -->
<!-- start examples -->
### Example usage to upload chart on release
```yaml
name: Upload Released Chart
on:
  release:
    types:
      - published
jobs:
  upload-chart-gar:
    runs-on: ubuntu-latest
    steps:
      - name: Push Chart
        uses: swarm-io/action-upload-chart-gar@v1
        with:
          credentials-json: ${{ secrets.GAR_WRITE_SERVICE_ACCOUNT_KEY }}
          project-id: ${{ secrets.GCLOUD_PROJECT_ID_PROD }}
```
<!-- end examples -->
<!-- start [.github/ghdocs/examples/] -->
<!-- end [.github/ghdocs/examples/] -->
