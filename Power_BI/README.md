# Power BI resources for VIVO

This folder contains Power BI templates and example reports for analysing data from a VIVO instance.

Two approaches are provided:

- **RDBMS-style data access** – uses predefined VIVO data distributors that expose tabular datasets suitable for building reusable Power BI semantic models and reports.
- **Focused SPARQL reports** – uses report-specific data distributors and Power BI templates for particular analyses, such as publication trends, collaborations, funding, research areas, and publication venues.

## Folder structure

- `Templates/RDBMS/` – reusable Power BI templates based on the RDBMS-style VIVO data distributors.
- `Examples/RDBMS/` – example Power BI files created from the RDBMS-style templates.
- `Templates/SPARQL/` – Power BI templates for individual analytical use cases.
- `Examples/SPARQL/` – example Power BI reports and PDF previews for these use cases.

## Getting started

Before opening the Power BI templates, install the required VIVO data distributors.

For the RDBMS approach, upload [`RDBMS_distributors.n3`](../Distributors/RDBMS_distributors.n3) into the VIVO display model.

For the SPARQL-based reports, upload [`custom_distributors.n3`](../Distributors/custom_distributors.n3) into the VIVO display model.

In both cases, the distributors can be installed via:

**Site Admin → Ingest Tools → Manage Jena Models → Configuration Models**

Use the **add/remove RDF data** option for the display model.

After the distributors are installed:

1. Open the appropriate `.pbit` file in Power BI Desktop.
2. Enter the URL of your VIVO instance when prompted.
3. Provide credentials if your VIVO Data Distribution API requires authentication.
4. Load or refresh the data.
5. Save the configured report as a `.pbix` file if you want to reuse it.

The files under `Examples/` illustrate the expected result and can be used as a reference when creating your own reports.

## Which approach should I use?

Use the **RDBMS-style approach** if you want a broader reusable dataset and plan to create several analyses or reports from the same VIVO data.

Use the **focused SPARQL approach** if you need a specific analytical view and want to start from one of the prepared report templates.

## Additional tools

The repository also contains Python scripts in the [`scripts`](../scripts/) folder that can retrieve data exposed by the RDBMS distributors and make it available to Python or export it to Excel.

## Documentation

For detailed instructions and background, see the VIVO documentation:

- [VIVO Data in Power BI](https://wiki.lyrasis.org/spaces/VIVODOC116x/pages/461472832/VIVO+Data+in+Power+BI)
- [VIVO for Data Analysts](https://wiki.lyrasis.org/spaces/VIVODOC116x/pages/364742364/VIVO+for+Data+Analysts)

The first page explains the Power BI integration in more detail, while the second provides broader background on extracting and analysing VIVO data.