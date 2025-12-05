# Drouot Scraper
>This scraper pulls structured, high-quality auction data from Drouot.com, one of Europe’s most active art marketplaces. It captures catalog details, bidding information, artwork metadata, and seller info directly from listing or search URLs—ideal for analysts, collectors, dealers, and art-market intelligence platforms.


<p align="center">
  <a href="https://bitbash.dev" target="_blank">
    <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/scraper.png" alt="Bitbash Banner" width="100%"></a>
</p>
<p align="center">
  <a href="https://t.me/Bitbash333" target="_blank">
    <img src="https://img.shields.io/badge/Chat%20on-Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram">
  </a>&nbsp;
  <a href="https://wa.me/923249868488?text=Hi%20BitBash%2C%20I'm%20interested%20in%20automation." target="_blank">
    <img src="https://img.shields.io/badge/Chat-WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" alt="WhatsApp">
  </a>&nbsp;
  <a href="mailto:sale@bitbash.dev" target="_blank">
    <img src="https://img.shields.io/badge/Email-sale@bitbash.dev-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail">
  </a>&nbsp;
  <a href="https://bitbash.dev" target="_blank">
    <img src="https://img.shields.io/badge/Visit-Website-007BFF?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Website">
  </a>
</p>

<p align="center" style="font-weight:600; margin-top:8px; margin-bottom:8px;">
  Created by Bitbash, built to showcase our approach to Scraping and Automation!<br>
  If you are looking for <strong> Drouot Scraper</strong> you've just found your team — Let's Chat. 👆👆
</p>


## Introduction
The project automates the extraction of detailed auction listings from Drouot, transforming scattered catalog pages into clean, structured JSON.  
It solves the difficulty of gathering consistent pricing ranges, lot descriptions, and auction statuses manually and supports anyone studying trends or building valuation tools.

### What You Get From It
- Complete artwork and lot metadata  
- Pricing ranges, bidding activity, and auction status  
- Images and catalog references  
- Seller and contact information  
- Scalable crawling for long catalog lists  

---
## Features
| Feature | Description |
|---------|-------------|
| Artwork Metadata Extraction | Retrieves lot names, descriptions, categories, edition notes, signatures, provenance, and more. |
| Auction Data Capture | Extracts estimate ranges, bidding levels, reserve price info, and auction timing. |
| Image Collection | Saves all artwork images including the main catalog image. |
| Seller Information | Pulls seller or auction house contact details. |
| Search-URL Crawling | Works from any listing or search page to fetch multiple lots at once. |
| Structured JSON | Clean output ready for databases, pricing models, or dashboards. |

---
## What Data This Scraper Extracts
| Field Name | Field Description |
|------------|-------------------|
| lot_number | SKU / lot identifier for the artwork. |
| title | Artwork or object name. |
| description | Full catalog description including technique, condition, and notes. |
| category | Classification (e.g., Painting, Sculpture, Photography). |
| images | Array of all extracted image URLs. |
| main_image | Primary catalog image. |
| estimate_low | Lower price estimate. |
| estimate_high | Higher price estimate. |
| current_bid | Current highest bid if available. |
| next_bid | Required next bid amount. |
| reserve_met | Indicates if the reserve price was met. |
| auction_type | Online or live auction. |
| auction_status | Status such as ongoing, closed, or upcoming. |
| start_time | Auction start timestamp. |
| end_time | Auction end timestamp. |
| seller_name | Auction house or seller. |
| seller_contact | Contact details extracted from the catalog page. |

---
## Example Output
    
    [
      {
        "lot_number": "153",
        "title": "Bernard Buffet — Nature morte au vase",
        "description": "Oil on canvas, signed and dated 1963. Good condition. Provenance noted.",
        "category": "Peinture",
        "images": [
          "https://example.com/img1.jpg",
          "https://example.com/img2.jpg"
        ],
        "main_image": "https://example.com/img1.jpg",
        "estimate_low": 12000,
        "estimate_high": 18000,
        "current_bid": 14500,
        "next_bid": 15000,
        "reserve_met": true,
        "auction_type": "online",
        "auction_status": "in progress",
        "start_time": "2024-05-12T09:00:00Z",
        "end_time": "2024-05-19T18:00:00Z",
        "seller_name": "Maison de Ventes Dupont",
        "seller_contact": "+33 1 44 22 00 00"
      }
    ]

---
## Directory Structure Tree
    
    drouot-scraper/
    ├── src/
    │   ├── main.js
    │   ├── crawler/
    │   │   ├── playwright_engine.js
    │   │   ├── pagination.js
    │   │   └── extractors.js
    │   ├── utils/
    │   │   ├── logger.js
    │   │   ├── formatting.js
    │   │   └── validator.js
    │   └── config/
    │       └── input_schema.json
    ├── data/
    │   ├── sample_input.json
    │   └── sample_output.json
    ├── Dockerfile
    ├── package.json
    └── README.md

---
## Use Cases
- **Art market analysts** track pricing trends, estimate accuracy, and bidding behavior.  
- **Auction houses** compare their catalogs with competitors and monitor artist popularity.  
- **Dealers and collectors** evaluate artworks, provenance, and historical bidding patterns.  
- **Data platforms** enrich valuation tools and price databases with structured auction insights.  
- **Researchers** study trends across categories, artists, or sale cycles.

---
## FAQs

**Can it scrape entire auction catalogs?**  
Yes—when given a search or category URL, it crawls all available lots.

**Does it retrieve high-resolution images?**  
It extracts all image URLs; quality depends on what Drouot provides.

**What if a page has missing pricing info?**  
Fallback extraction rules keep the JSON structure stable even with incomplete fields.

**Can this be used for real-time bidding analysis?**  
It captures current bids and status but is not meant for automated bidding systems.

---
### Performance Benchmarks and Results

**Primary Metric:**  
Efficiently crawls dozens of catalog lots per minute while preserving detailed metadata.

**Reliability Metric:**  
Consistently handles mixed content formats and varying catalog layouts.

**Efficiency Metric:**  
Optimized Playwright workflows reduce page-load overhead for large search crawls.

**Quality Metric:**  
High metadata completeness with robust parsing for images, pricing, and auction states.



---


<p align="center">
<a href="https://calendar.app.google/74kEaAQ5LWbM8CQNA" target="_blank">
  <img src="https://img.shields.io/badge/Book%20a%20Call%20with%20Us-34A853?style=for-the-badge&logo=googlecalendar&logoColor=white" alt="Book a Call">
</a>
  <a href="https://www.youtube.com/@bitbash-demos/videos" target="_blank">
    <img src="https://img.shields.io/badge/🎥%20Watch%20demos%20-FF0000?style=for-the-badge&logo=youtube&logoColor=white" alt="Watch on YouTube">
  </a>
</p>
<table>
  <tr>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/MLkvGB8ZZIk" target="_blank">
        <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/review1.gif" alt="Review 1" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        "Bitbash is a top-tier automation partner, innovative, reliable, and dedicated to delivering real results every time."
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Nathan Pennington
        <br><span style="color:#888;">Marketer</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/8-tw8Omw9qk" target="_blank">
        <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/review2.gif" alt="Review 2" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        "Bitbash delivers outstanding quality, speed, and professionalism, truly a team you can rely on."
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Eliza
        <br><span style="color:#888;">SEO Affiliate Expert</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/m-dRE1dj5-k?si=5kZNVlKsGUhg5Xtx" target="_blank">
        <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/review3.gif" alt="Review 3" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        "Exceptional results, clear communication, and flawless delivery. <br>Bitbash nailed it."
      </p>
      <p style="margin:1px 0 0; font-weight:600;">Syed
        <br><span style="color:#888;">Digital Strategist</span>
        <br><span style="color:#f5a623;">★★★★★</span>
         </p>
