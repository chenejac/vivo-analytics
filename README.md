# VIVO Analytics

This repository contains reusable resources for extracting, analysing, and visualising data from VIVO. It is intended for data analysts and VIVO administrators who want to use VIVO data in tools such as Microsoft Power BI or Excel.

## Repository contents

### Data distributors

The [`Distributors`](Distributors/) directory contains VIVO Data Distribution API definitions:

- [`RDBMS_distributors.n3`](Distributors/RDBMS_distributors.n3) – a set of distributors that expose commonly used VIVO entities and relationships as tabular data suitable for relational-style analysis.
- [`custom_distributors.n3`](Distributors/custom_distributors.n3) – examples of custom distributors that can be adapted for specific analytical needs.

These distributors are intended to be installed in a VIVO instance and accessed through the VIVO Data Distribution API. To install them, upload the corresponding .n3 file into the VIVO display model via Site Admin → Ingest Tools → Manage Jena Models → Configuration Models, using the add/remove RDF data option for the display model. For detailed installation and usage instructions, see [VIVO Data in Power BI](https://wiki.lyrasis.org/spaces/VIVODOC116x/pages/461472832/VIVO+Data+in+Power+BI).

### Power BI resources

The [`Power_BI`](Power_BI/) directory contains Power BI templates and examples for two approaches:

- **RDBMS-style model** – uses the predefined VIVO distributors to load a broader set of related tables into a reusable Power BI semantic model.
- **SPARQL-specific reports** – focused Power BI reports that retrieve the data required for a particular analysis.

The directory contains both reusable `.pbit` templates and `.pbix` examples. Some example reports also include PDF previews.

See [`Power_BI/README.md`](Power_BI/README.md) for a short usage guide.

### Export scripts

The [`scripts`](scripts/) directory contains small Python examples for retrieving distributor output:

- [`vivo_to_power_bi.py`](scripts/vivo_to_power_bi.py) – loads the configured VIVO distributors into pandas data frames for use with Power BI/Python workflows.
- [`vivo_to_excel.py`](scripts/vivo_to_excel.py) – exports the distributor output to an Excel workbook.

## Getting started

A typical workflow is:

1. Make sure the required Data Distribution API distributors are available in your VIVO installation.
2. Choose either the RDBMS-style Power BI model or one of the focused SPARQL report templates.
3. Open the appropriate `.pbit` file in Power BI Desktop and configure it to use your VIVO instance and credentials when prompted.
4. Refresh the data and save the resulting report as a `.pbix` file.
5. Adapt the queries, model, and visualisations to your local VIVO data and reporting requirements.

The supplied `.pbix` files are examples showing what the corresponding templates can produce; for connecting to another VIVO instance, start with the `.pbit` templates.

## Documentation

For detailed instructions and background, see the VIVO documentation:

- [VIVO Data in Power BI](https://wiki.lyrasis.org/spaces/VIVODOC116x/pages/461472832/VIVO+Data+in+Power+BI)
- [VIVO for Data Analysts](https://wiki.lyrasis.org/spaces/VIVODOC116x/pages/364742364/VIVO+for+Data+Analysts)

The first page explains the Power BI integration in more detail, while the second provides broader background on extracting and analysing VIVO data.

## License

See the [`LICENSE`](LICENSE) file for licensing information.
