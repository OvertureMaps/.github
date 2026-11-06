## Welcome to the Overture Maps Foundation 🌍

<p align="center"><img src="./overture_maps_foundation_banner.png" width="450" alt="Overture Maps Foundation banner" /></p>

The [Overture Maps Foundation](https://overturemaps.org) is a Linux Foundation initiative producing free, open, and interoperable map data for developers and organizations worldwide. Our datasets cover the core [themes](https://docs.overturemaps.org/schema/) of the physical world: addresses, buildings, divisions, places, transportation, and base features, released as cloud-native GeoParquet files, versioned and ready to build on.

## 🗺️ Data & Schema

| Repository | Description |
| :--- | :--- |
| [data](https://github.com/OvertureMaps/data) | Overture data releases: access scripts, cloud paths, and release notes |
| [schema](https://github.com/OvertureMaps/schema) | The canonical Overture schema specification |
| [docs](https://github.com/OvertureMaps/docs) | Documentation site, published at [docs.overturemaps.org](https://docs.overturemaps.org) |
| [stac](https://github.com/OvertureMaps/stac) | Creates manifest files for cataloguing Overture releases, published at [stac.overturemaps.org](https://stac.overturemaps.org) |
| [overture-providers](https://github.com/OvertureMaps/overture-providers) | Public provider registry and dataset configs for Overture data sources |

## 🛠️ Developer Tools

| Repository | Description |
| :--- | :--- |
| [overturemaps-py](https://github.com/OvertureMaps/overturemaps-py) | Python CLI and library for downloading and working with Overture data |
| [overture-tiles](https://github.com/OvertureMaps/overture-tiles) | Generate PMTiles archives from Overture data |
| [explore-site](https://github.com/OvertureMaps/explore-site) | Interactive map explorer for Overture data themes |
| [osm-pbf-parquet](https://github.com/OvertureMaps/osm-pbf-parquet) | Transcode OSM PBF files to hive-partitioned Parquet |
| [transportation-splitter](https://github.com/OvertureMaps/transportation-splitter) | PySpark tool for splitting Overture transportation segments |
| [transportation-routing](https://github.com/OvertureMaps/transportation-routing) | Tools and documentation for routing with Overture transportation data |
| [terraform-aws-overture-tiles](https://github.com/OvertureMaps/terraform-aws-overture-tiles) | Terraform/Tofu module for generating PMTiles of Overture data on AWS |
| [stac-check-action](https://github.com/OvertureMaps/stac-check-action) | Unofficial GitHub Action to run [stac-check](https://github.com/stac-utils/stac-check) for linting and best practices |
| [overture-core](https://github.com/OvertureMaps/overture-core) | Shared SDK: bundle and provenance model, config, check framework, platform abstractions, and registry client |
| [overture-airflow-provider](https://github.com/OvertureMaps/overture-airflow-provider) | Apache Airflow provider for the services Overture uses |
| [matchers](https://github.com/OvertureMaps/matchers) | Python matchers used by OMF to conflate data |

## 📚 Learning & Community

| Repository | Description |
| :--- | :--- |
| [workshop](https://github.com/OvertureMaps/workshop) | Demos and workshop notebooks for working with Overture data and GERS |
| [awesome-gers](https://github.com/OvertureMaps/awesome-gers) | A curated list of projects, tools, and resources built with GERS |
| [workflows](https://github.com/OvertureMaps/workflows) | Reusable GitHub Actions workflows for the OvertureMaps organization |

---

Exploring experimental projects and apps? Check out [labs.overturemaps.org](https://labs.overturemaps.org) for our Labs initiatives.

Questions or ideas? Open an issue in the relevant repository, or visit [overturemaps.org](https://overturemaps.org) to learn more. 💙
