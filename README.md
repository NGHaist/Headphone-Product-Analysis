# Headphone Product Analysis

## Project Overview

This project analyzes publicly available Amazon customer ratings and reviews for a well-known Bluetooth headphone product to identify sentiment patterns, recurring themes, and broader consumer insights. The specific brand and product name are intentionally redacted from most public-facing materials for ethical reasons, given the project’s unofficial and educational nature.

The primary goal is to practice and demonstrate **exploratory data analysis (EDA)** and insight extraction using **Python, SQL, AI-driven text analysis, and data visualization**, while adhering to responsible and ethical data collection practices.

For analytical purposes, all color and minor product variants are treated as a **categorical dimension** rather than as separate products.


## Project Scope

* **Marketplace:** Amazon (public review pages only)
* **Variants:** All available color options
* **Unit of Analysis:** One individual customer review
* **Time Coverage:** Entire review history available at scrape time


## Out of Scope

The following data is explicitly excluded:

* Reviewer identity or demographics
* Review images or videos
* Seller responses
* Pricing or sales data
* Competitor products


## Data Fields Collected

The following review-level fields are collected:

| Field Name          | Data Type     | Description                       |
| ------------------- | ------------- | --------------------------------- |
| `review_id`         | Text          | Unique identifier for each review |
| `product_id`        | Text          | Amazon product identifier (ASIN)  |
| `review_title`      | Text          | Review headline                   |
| `review_text`       | Text          | Full review body                  |
| `star_rating`       | Integer (1–5) | User-selected rating              |
| `review_date`       | Date          | Date the review was posted        |
| `verified_purchase` | Boolean       | Amazon verified purchase flag     |
| `helpful_votes`     | Integer       | Number of helpful votes           |
| `variant_color`     | Text          | Color variant purchased           |

**Note:** Reviewer display names are intentionally excluded to minimize unnecessary personal data collection and because they are not required for analysis.


## Analytical Rationale

Each collected field supports downstream analytical goals:

* **Star ratings** provide a quantitative baseline for sentiment
* **Review text** enables AI-driven sentiment and topic extraction
* **Verified purchase status** helps filter potentially unreliable reviews
* **Helpful votes** approximate a review’s visibility and influence
* **Color variants** enable within-product comparative analysis
* **Review dates** support time-series and product lifecycle analysis

