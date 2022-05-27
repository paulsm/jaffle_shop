## Testing dbt project: `bake_shop`

`bake_shop` is a fictional ecommerce store. This dbt project transforms raw data from an app database into a customers and orders model ready for analytics.

### What is this repo?
What this repo _is_:
- A self-contained playground dbt project, useful for testing out scripts, and communicating some of the core dbt concepts to demonstrate how to use dbt with WANdisco LiveData Hub.

What this repo _is not_:
- A tutorial — check out the [Getting Started Tutorial](https://docs.getdbt.com/tutorial/setting-up) for that. Notably, this repo contains some anti-patterns to make it self-contained, namely the use of seeds instead of sources.
- A demonstration of best practices — check out the [dbt Learn Demo](https://github.com/dbt-labs/dbt-learn-demo) repo instead. We want to keep this project as simple as possible. As such, we chose not to implement:
    - our standard file naming patterns (which make more sense on larger projects, rather than this five-model project)
    - a pull request flow
    - CI/CD integrations
- A demonstration of using dbt for a high-complex project, or a demo of advanced features (e.g. macros, packages, hooks, operations) — we're just trying to keep things simple here!

### What's in this repo?
This repo contains [seeds](https://docs.getdbt.com/docs/building-a-dbt-project/seeds) that includes some example raw data from a fictional app.

The raw data consists of customers, orders, and payments, with the following entity-relationship diagram:

![Bake Shop ERD](/etc/jaffle_shop_erd.png)


### Running this project
To get up and running with this project:
1. Reference this project as an endpoint in LiveData Hub.

2. Create an endpoint for your chosen data platform, e.g. Databricks or Snowflake.

3. Create a LiveData Hub Transformation, using this project and a trigger based on the arrival of new data into the target cloud storage of your choice.
