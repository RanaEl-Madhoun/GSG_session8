# Session 7 Practice — Key Findings

This notebook explores three public datasets—online chess games, the Netflix catalog, and global monthly temperature anomalies—and exports charts to `output/charts/`. Below are five conclusion-first findings drawn from the analysis. Each claim is tied to a saved chart.

---

## 1. Resignation is the dominant way chess games end.

More than half of all recorded games in the sample conclude by resignation rather than checkmate, timeout, or draw. Resignations account for roughly 56% of outcomes, with White winning about 5,844 resignations and Black about 5,303—far exceeding mate or out-of-time finishes for either side. Draws occur in only 906 games and almost never coincide with a decisive winner label. **Implication:** at this skill level, players tend to concede once the position is lost instead of playing to forced mate or the clock. **Chart:** `chess_victory_status_barplot.png`

## 2. White ratings in the corpus sit above the 1500 baseline and trend upward over the game sequence.

The typical White player enters near 1,597 Elo, and about 63% of games feature a White rating at or above 1500. The rolling 10-game mean tracks a gradual rise through the sorted game IDs, with visible stretches above the reference line filled in red on the time-series plot. Peak ratings reach 2,700, indicating occasional expert-level players in an otherwise club-strength pool. **Implication:** the dataset skews toward rated, competitive play rather than casual beginners. **Chart:** `chess_white_rating_timeseries.png`

## 3. The United States overwhelmingly leads Netflix’s country footprint.

After splitting multi-country production labels, the United States accounts for 3,689 titles—more than three times India (1,046) and more than four times the United Kingdom (804). Canada, France, Japan, and Spain follow at much lower counts. **Implication:** Netflix’s catalog is heavily U.S.-centric in stated origin, even as the platform markets globally. **Chart:** `netflix_top10_countries.png`

## 4. Netflix shifted from a movie-heavy catalog toward parity with TV between 2013 and 2021.

Movie releases peaked in 2017–2018 (767 titles per year) while TV Show additions accelerated steadily, rising from 63 in 2013 to 436 in 2020. TV’s share of annual releases grew from roughly 22% in 2013 to about 53% in 2021, even as total new titles fell after 2019. **Implication:** Netflix’s growth strategy in this period prioritized serial content and international series over theatrical-style volume. **Chart:** `netflix_movies_tv_stacked_bar.png`

## 5. Global temperature anomalies have warmed sharply decade over decade since 1950.

Monthly anomalies were near zero or negative in the 1950s–1970s but turned consistently positive from the 1990s onward. Mean anomaly climbed from about 0.35 °C in the 1990s to 0.55 °C in the 2000s, 0.77 °C in the 2010s, and 1.02 °C in the 2020s (partial decade). The heatmap shows winter and spring months warming as much as summer bands in recent decades, with deep red cells across all months in the 2010s and 2020s columns. **Implication:** warming is broad-based across seasons, not limited to a single month, and the pace accelerates in the most recent decades. **Chart:** `global_temp_heatmap.png`

---

**Data sources:** chess games (local CSV), Netflix titles (local CSV), global monthly temperature ([GitHub dataset](https://github.com/datasets/global-temp)). Processed tables are in `output/data/`; figures are in `output/charts/`.
