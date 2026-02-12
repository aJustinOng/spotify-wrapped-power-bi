# Spotify Wrapped in Power BI ![PowerBI](./assets/img/spotify.svg)

**Skills:** `Data ETL | Data Visualization | DAX | 3rd Party Web API`

**Tools:** `Power BI | Power Query`

##### [See my other projects!](https://github.com/aJustinOng)

---

## Overview

Spotify Wrapped is a popular online phenomenon that pops up every year, but it is inherently incomplete, as data is often cut by mid November to generate the summary before the year ends. In this project, I reconstructed and customized Spotify Wrapped using Spotify’s provided personal data and public Web API, producing a extensive view of the classic report that can span multiple years.

<img src="/assets/img/project-spotify-wrapped-power-bi-dashboard.gif" width="100%"/>

Using Power Query, hundreds of thousands of streaming records are ingested from raw, local JSON files and transformed into a structured semantic model. After basic cleaning, unique track and artist identifiers are grouped into controlled batches to be queried to the [Spotify Web API](https://developer.spotify.com/). Through the Web API, the model can obtain additional resources like album and artist images and genre information. To prevent exceeding rate limits, the most relavant tracks and artists are targeted and grouped for batch querying, reducing ~25000 single queries to just 33 API calls.

<img src="/assets/img/project-spotify-wrapped-power-bi-power-query.png" width="100%"/>

The result is a fully reproducible, end-to-end analytics pipeline that combines raw data, API-based enrichment, and analytical modeling to recreate — and extend — Spotify Wrapped with greater accuracy, completeness, and analytical flexibility.

**Note:** According to [official Spotify documentation](https://developer.spotify.com/documentation/web-api), API calls in the future will require a premium Spotify account.
