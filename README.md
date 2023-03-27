# haproxy2sql
HAProxy Logging to PostgresSQL via Fluent




# Postgres Schema
```
DROP TABLE haproxy;
CREATE TABLE haproxy (
    id serial PRIMARY KEY NOT NULL,
    timestamp TIMESTAMP WITH TIME ZONE NOT NULL,
    ip INET,
    method TEXT,
    url TEXT,
    code SMALLINT,
    bytes INTEGER,
    useragent TEXT,
    auth CHAR (32),
    referer TEXT,
    ttfb INTEGER
);
```
