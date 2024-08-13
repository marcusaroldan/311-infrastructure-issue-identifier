# 311-infrastructure-issue-identifier
The purpose of this repo is to collect and classify illegal parking reports to identify infrastructure issues around Boston.
The notebooks contained within this repo form the full data pipeline, from collecting the illegal parking reports from the Boston 311 API, to classifying these reports, to processing them for visualization. Currently, there is a prototype visualization available at [this link](https://marcusaroldan.github.io/311-infrastructure-issue-identifier/).

Important Files:
- [`infrastructure-issue-identifier.ipynb`](infrastructure-issue-identifier.ipynb):
This notebook takes in raw service request data and categorizes it according to the classification scheme contained within it. The notebook then repackages the classified documents, adding classification and keyword match information.

- [`infrastructure-issues-map-preprocess.ipynb`](infrastrucutre-issues-map-preprocess.ipynb):
This notebook converts categorized service requests (output file of `infrastructure-issue-identifier.ipynb`) into GeoJSON format for display.

- [`data/infra_issues.geojson`](data/infra_issues.geojson):
Example result file of `infrastructure-issues-map-preprocess.ipynb`.

- [`data/infra_issues.json`](data/infra_issues.json):
Example result file of `infrastructure-issue-identifier.ipynb`.

- [`data/service_requests.json`](data/service_requests.json):
Example result file of `collect-new-service-reports.ipynb`.
