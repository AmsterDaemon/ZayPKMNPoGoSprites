## Disclaimer
This project contains visual assets (sprites) originating from Pokémon GO.
I am not affiliated with Pokémon GO, The Pokémon Company, Niantic, or Scopely.
All Pokémon-related assets, names, and intellectual property belong to their respective owners.

## About This Project
This project is an independent, fan-made tool. I have built my own Pokémon GO calculator and data cache that allows users to upload an appraisal screenshot and automatically calculate:
- The Pokémon’s current level
- Pokéstop Showcase score
- Best possible PvP league rankings

League results are filtered to exclude leagues the Pokémon cannot legally enter due to CP limits, including evolution constraints.

This project is intended for educational and quality-of-life purposes only and is not meant to compete with or replace Pokémon GO.

## Motivation & Vision
As the project evolved, it became clear that Pokémon GO exposes far more meaningful information than most players are able to actively use. What started as an exploration of that hidden-in-plain-sight data quickly grew into a broader idea: helping players turn raw information into insight.

My goal is not just to calculate numbers, but to help players make better decisions, such as:
- which Pokémon to keep or transfer  
- which Pokémon are worth evolving or powering up  
- which league a Pokémon is best suited for  
- which Pokémon to prioritize catching during events  
- and where to focus resources such as XL Candy  

In short, PoGOCR aims to help players define and pursue goals they may not have realized were achievable within Pokémon GO. *Maybe you'll catch a rank 1 PvP Pokémon without even realizing it?*

At the moment, this project runs locally and does not store data for other users. 
My next goal is to introduce user accounts, allowing players to build their own personal collections — not only for themselves, but also to share with others.

This opens the door to a more social experience: comparing collections, showing off shiny catches of the day, tracking progress over time, and surfacing meaningful highlights instead of raw lists.

Long-term, PoGOCR is envisioned as a personal Pokémon GO companion — a place where players can analyze their collection, understand their strengths, and engage with the community around shared goals and discoveries, while remaining independent of in-game limitations.

If this project sparks ideas or highlights quality-of-life improvements that could benefit Pokémon GO itself, that would be a welcome outcome.

## Core Features

- **Screenshot-based data ingestion**  
  Upload Pokémon GO appraisal screenshots to extract IVs, CP, HP, height, weight, form, and other relevant metadata.

- **Accurate Pokémon level calculation**  
  Determines a Pokémon’s current level using CP, IVs, and species-specific base stats.

- **Pokéstop Showcase scoring**  
  Calculates showcase scores with correct handling of size classes (XXS–XXL) and species-specific size ranges.

- **PvP league ranking analysis**  
  Evaluates the Pokémon’s best possible PvP performance across leagues, automatically excluding:
  - leagues it cannot legally enter due to CP limits  
  - invalid evolutions that would exceed league caps  

- **Form- and evolution-aware logic**  
  Supports regional forms, special forms, and evolution chains when calculating rankings and eligibility.

- **User collections & saved data**  
  Uploaded Pokémon can be saved to a user account, forming a persistent personal collection that can be searched, filtered, and analyzed.

- **Manual review & validation**  
  OCR results can be reviewed and corrected, with visual indicators when inferred values conflict with known game constraints.

- **Fully self-contained calculations**  
  All calculations are performed using custom logic and datasets, without relying on third-party PvP or ranking services.

## Tech Stack

### Frontend
- **Vue 3**
- **JavaScript (ES modules)**
- **HTML5 / CSS3**
- Component-based UI with dynamic filtering, highlighting, and interactive editors

### Backend
- **Node.js**
- **Express.js**
- REST-style API for image uploads, OCR processing, calculations, and user data management

### OCR & Image Processing
- **Tesseract OCR**
- Screenshot preprocessing and normalization
- Metadata extraction and validation pipelines

### Data & Logic
- Custom Pokémon GO calculation engine:
  - CP & level calculations
  - PvP league rankings
  - Pokéstop Showcase scoring
- Species, form, and evolution datasets maintained independently
- Structured JSON-based storage with database-backed persistence for user accounts

### Platform Design Principles
- Web-first, account-based platform
- Designed for long-term personal collection tracking
- No reliance on external PvP or ranking APIs
- Transparent, debuggable calculation logic
- Built to scale from individual players to a broader community

## Roadmap

### Short-term
- Improve OCR accuracy and edge-case handling  
- Expand validation rules for CP, HP, and evolution constraints  
- Performance optimizations for screenshot processing  
- UI improvements for faster reviewing and editing of uploads  

### Mid-term
- User accounts and authentication  
- Persistent personal Pokémon collections  
- Advanced filtering and search across collections  
- Event-aware insights:
  - identifying high-value spawns during active events  
  - surfacing top IV or showcase-relevant Pokémon  

### Long-term
- Deeper collection analytics and historical insights  
- Smarter decision-support tooling (beyond raw calculations)  
- Enhanced Pokéstop Showcase optimization features  
- Continued exploration of quality-of-life improvements Pokémon GO does not currently expose
