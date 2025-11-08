# Projekat 2: Customer Personality Analysis - Klasterizacija Kupaca

Ovaj projekat je realizovan u okviru predmeta **Mašinsko učenje**.

**Autori:** Aleksandar Pešić, Mladen Nikolić

## Tema: Nenadgledano učenje - Klasterizacija

### Problem
Cilj projekta je segmentacija kupaca na osnovu njihovih demografskih karakteristika, ponašanja pri kupovini i odgovora na marketing kampanje. Kroz klasterizaciju, identifikujemo različite grupe (persone) kupaca kako bismo omogućili personalizovane marketing strategije.

### Skup podataka (Dataset)
Korišćen je javno dostupan "Customer Personality Analysis" dataset sa Kaggle-a.
[Link do dataseta](https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis/data)

### Metodologija
Projekat prati standardni pipeline za nenadgledano učenje:
1.  **Učitavanje i Istraživanje Podataka (EDA):** Uvid u osnovne statistike i distribucije.
2.  **Priprema Podataka (Data Preprocessing):**
3.  **Inženjering Atributa (Feature Engineering):** Kreiranje novih, smislenijih atributa.
4.  **Skaliranje:** Korišćenje `StandardScaler`-a da se atributi dovedu na istu skalu, što je ključno za PCA i K-Means.
5.  **Redukcija Dimenzionalnosti:** Primena `PCA` (Analiza glavnih komponenti) za smanjenje broja atributa uz očuvanje većine varijanse (>=90%).
6.  **Modeliranje (Klasterizacija):**
    * Određivanje optimalnog broja klastera (K) pomoću *Elbow*, *Silhouette* i *Davies-Bouldin* metoda.
    * Primena i poređenje četiri različita algoritma: **K-Means**, **Agglomerative Clustering (Hijerarhijsko)**, **DBSCAN** i **Gaussian Mixture Models (GMM)**.
7.  **Evaluacija i Profilisanje:** Analiza dobijenih klastera, vizualizacija (PCA, t-SNE, Box-plotovi) i definisanje profila za svaku grupu kupaca.