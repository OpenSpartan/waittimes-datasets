<div align="center">
	<br>
	<br>
	<div>
		<picture>
			<img alt="OpenSpartan Wait Times Dataset Logo" width="200px" src="media/logo.png">
		</picture>
		<br>
	</div>
	<h1>OpenSpartan Wait Times Datasets</h1>
	<p>
		An open-source dataset of Halo Infinite wait times powered by <a href="https://openspartan.com">OpenSpartan</a> tooling.
	</p>
	<br>
	<br>
	<br>
</div>


# Overview

This repository contains historical data sets for Halo Infinite match times, as captured from the **United States west coast**.

While the data is not necessarily capturing the _global_ wait times, it can be used as a reasonable reference point for wait times for various playlists available through each of the Halo Infinite operations since the start of tracking on the OpenSpartan side.

## Datasets

| 🎖️ Event/Operation | 📆 Timeframe                     | 📦 Dataset                        | 📝 Notes                                                               |
|:----------------|:------------------------------|:-------------------------------|:-------------------------------------------------------------------|
| [Banished Honor](https://www.halowaypoint.com/news/banished-honor-operation-launch) | April 30, 2024 - June 4, 2024 | [`banished-honor-wait-times.db`](datasets/banished-honor-wait-times.db) | Data has a few gaps as data collection tool issues were addressed. |
| [Tenrai IV](https://www.halowaypoint.com/news/tenrai-iv-operation-launch) | June 4, 2024 - July 2, 2024   | [`tenrai-iv-wait-times.db`](datasets/tenrai-iv-wait-times.db)      | Data has a few gaps as data collection tool issues were addressed. |
| [Anvil](https://www.halowaypoint.com/news/anvil-operation-launch)           | July 2, 2024 - July 30, 2024  | _In progress_                  | Data collection is currently in progress.                          |

## Analyzing the data

Every single dataset available in this repository is a [SQLite database](https://www.sqlite.org/). You can query it from any language or framework that supports SQLite, and even make pretty graphs with [Jupyter notebooks](https://jupyter.org/) and [Python](https://www.python.org/).

There are two tables in each datasets:

| Table | Description |
|:------|:------------|
| `PlaylistMetadata`  | Outlines all playlist-related metadata, including playlist asset ID, version ID, name, description, and more. |
| `WaitTimeSnapshots` | Captures playlist wait times, in 10 minute intervals. Data includes snapshot timestamp (PT time zone), asset ID, version ID, and wait time in seconds. |

You can also analyze the data with the help of a tool like [DB Browser for SQLite](https://sqlitebrowser.org/).

![DB Browser for SQLite used to parse the OpenSpartan Wait Times Datasets](media/db-browser-sqlite.gif)
