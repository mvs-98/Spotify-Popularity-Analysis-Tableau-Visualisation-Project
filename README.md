---

# **Spotify Popularity Analysis – Tableau Visualisation Project**

This repository contains a Tableau dashboard exploring artist and genre popularity using the Spotify dataset.
The goal of this project is to identify the most popular artists and genres, understand the relationship between popularity and song count, and create an interactive dashboard for deeper exploration.

---

## **Dataset**

The dataset includes various song-level metrics from Spotify, including:

* Artist
* Genre
* Popularity
* Track-level data

This dataset was imported into Tableau using the **Connect to a File → Microsoft Excel** option.

---

## **Visualisations Created**

### **1. Popular Artists (Top 20) – Bar Chart**

This chart identifies the top 20 most popular artists using multiple approaches.

**Key steps:**

* Dragged **Artist** into the Rows shelf.
* Used **AVG(Popularity)** to determine artist performance.
* Filtered to **Top 20** artists by popularity.
* Sorted artists in descending order based on popularity.
* Created an additional stacked bar chart using **SUM(Popularity)** to visualise top artists along with their associated genres.

**Outcome:**
A clear comparison of the most popular artists based on both average and cumulative popularity values.

---

### **2. Popular Genres – Bar Chart**

This visualisation identifies the most popular genres based on cumulative popularity.

**Key steps:**

* Dragged **Genre** to Rows.
* Added **SUM(Popularity)** to Columns.
* Sorted genres to show the most popular clearly.

**Outcome:**
A ranking of genres based on total popularity.

---

### **3. Impact of Song Count on Genre Popularity**

**Question:**
*Is genre popularity influenced by the number of songs in that genre?*

**Approach:**

* Created a **calculated field** to count the number of songs per genre.
* Built a visual showing **genre popularity vs. song count**.

**Outcome:**
A clear comparison revealing whether popularity is driven by volume of songs or listener preference.

---

### **4. Pie Charts for Top 20 Artists – Genre Breakdown**

For each of the top 20 artists, a pie chart was created showing the distribution of genres within their songs.

**Key steps:**

* Built a pie chart with **Genre** on Colour and **Popularity** as the measure.
* Sorted artists by **SUM(Popularity)**.
* Created a tooltip integration so that selecting an artist displays their genre composition.

**Outcome:**
Artist-specific genre insights integrated directly into the main artist popularity chart.

---

## **Dashboard – Spotify Popularity Explorer**

An interactive **Spotify Dashboard** was designed with the following components:

### **Dashboard Elements:**

* **Artist vs Popularity** (bar chart)
* **Artist vs Popularity – Pie Chart** (tooltip/hover interaction)
* **Popular Genres** (bar chart)
* **Genre Popularity vs Song Count** (comparison chart)

### **Interaction Features:**

* Hovering over an artist in the **Artist vs Popularity** chart automatically updates the **Pie Chart** to show that artist’s genre breakdown.
* Dynamic filtering for top artists and genres.
* Clean layout allowing users to explore both artist-level and genre-level insights.

---

## **Calculated Fields**

### **1. Song Count per Genre**

A calculated field was created to count number of songs in each genre:

```
COUNT([Genre])
```

Used to analyse correlation between genre popularity and song volume.

---

## **Key Insights (Findings)**

* **Drake** is the most popular artist when measured using both average and total popularity.
* **Pop** is the most popular genre based on cumulative popularity.
* **Genre popularity is not influenced by number of songs.**

  * Example: *Comedy* has the highest number of songs but is not the most popular genre.
* Genre popularity appears to be driven more by listener demand than genre volume.

---

## **Tools & Technologies**

* **Tableau Desktop** for visualisations
* **Spotify dataset (Excel)**
* Calculated fields, filters, stacked bar charts, pie charts, interactive tooltip integration, and dashboard design tools

---

## **Repository Structure**

```
/data                # Spotify dataset (if included)
/tableau             # Tableau workbook (.twbx)
README.md            # Project documentation
```

---

## **Summary**

This project provides:

* A multi-layered analysis of Spotify artist and genre popularity
* Interactive Tableau visualisations
* Correlation analysis between genre popularity and song count
* A user-friendly dashboard showcasing all insights

---
