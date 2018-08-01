Notebook for querying Aircloak Insights
=======================================

This R Studio notebook shows how one would go about querying
Aircloak Insights from R. Since Aircloak Insights provides a
Postgres Message Protocol interface implementation one can
query it using the R PostgresSQL driver as follows:

```{r}
library("RPostgreSQL")

drv  <- dbDriver("PostgreSQL")
conn <- dbConnect(drv, dbname = "<DATABASE>",
                 host = "<HOST>", port = 5432,
                 user = "<USER>",
                 password = "<PASSWORD>")
```
