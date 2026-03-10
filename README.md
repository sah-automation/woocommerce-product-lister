# Woocommerce Product Lister & Inventory Update System

An automated solution to scrape product data from supplier websites and list them on a WooCommerce store. This system streamlines the process of extracting complex product details, including variations, attributes, and high-quality images.

## 🚀 Features

- **Automated Web Scraping:** Uses Automa to extract deep product data (SKUs, titles, descriptions, images, specifications).
- **Variation Support:** Correctly handles variable products and their respective attributes (e.g., size, color, material).
- **Intermediate Data Storage:** Generates a structured CSV format for easy review and modification before listing.
- **WooCommerce Integration:** Utilizes the REST API (v3) to create and update products programmatically.
- **Category Mapping:** Includes logic to map supplier categories to specific WooCommerce category IDs.

## 📂 Project Structure

- `automa/`: Contains the `.automa.json` workflow file for browser-based data extraction.
- `data/`: Stores the intermediate CSV product listing data (`LuxeDecor2Woo-listing-data.csv`).
- `google-colab/`: Contains the Jupyter Notebook/Python code for processing the CSV and interacting with the WooCommerce API.

## 🛠️ Prerequisites

- **Automa Extension:** Installed in your web browser (Chrome/Firefox/Edge).
- **Python 3.x:** Installed locally or accessible via Google Colab.
- **WooCommerce Store:** Active WordPress site with the WooCommerce plugin.
- **API Credentials:** REST API `consumer_key` and `consumer_secret` from WooCommerce (Settings > Advanced > REST API).

## 🚦 Getting Started

### 1. Data Extraction (Scraping)
1. Open your browser and navigate to the **Automa Extension**.
2. Import the workflow from `automa/LuxeDecor2SC_Lister.automa.json`.
3. Configure the source URL (if necessary) and run the workflow.
4. Export the results to `data/LuxeDecor2Woo-listing-data.csv`.

### 2. Product Listing (WooCommerce)
1. Open the Jupyter Notebook in `google-colab/LuxeDecor2SC_Lister.ipynb`.
2. Update the `consumer_key` and `consumer_secret` variables with your WooCommerce API credentials.
3. Configure the `url` to match your WordPress site's REST API endpoint.
4. Run the notebook cells to process the CSV and upload your products.

## ⚖️ Legal & Ethical Compliance

**IMPORTANT:** This project is for **EDUCATIONAL PURPOSES ONLY**. 

- **Scraping Permissions:** Always obtain explicit permission from the supplier before scraping their website.
- **Terms of Service:** Ensure your use of this tool complies with the target website's Terms of Use.
- **Usage Policy:** The authors take no responsibility for any misuse of this tool or potential legal consequences.

See [ARCHITECTURE.md](ARCHITECTURE.md) for a detailed technical breakdown and further compliance information.

## 📜 License

This project is open-source and available under the MIT License.
