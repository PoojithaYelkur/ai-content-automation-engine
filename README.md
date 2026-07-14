# 🤖 Multi-Channel AI Social Media Content Engine

An automated, intelligent content distribution system built on **Make.com** using **Google Gemini 2.5 Flash**. This system monitors a centralized data source, structures complex technical updates, and formats personalized promotional assets dynamically across multiple community endpoints simultaneously.



---

## 🚀 How It Works

The architecture passes raw links through a tiered processing pipeline to generate platform-specific community posts:

1. **Trigger (Google Sheets):** Watches for new rows containing web links (e.g., public GitHub repositories, technical articles, portfolio links).
2. **Analysis (Gemini Summarizer):** Evaluates the web page context or codebase layout to extract core technical achievements, concepts, and key learnings.
3. **Distribution (Basic Router):** Automatically clones and passes the structured summary asset down three concurrent processing tracks.
4. **Platform Customization (Gemini Personalizers):** Three standalone Gemini operations dynamically adjust structural formatting, word lengths, and tones natively for respective target interfaces:
   * **LinkedIn Personalizer:** Focuses on an aspirational, career-relevant, tech-focused corporate summary.
   * **Facebook Personalizer:** Formats an engaging, conversational, community-driven hook utilizing custom emojis.
   * **Telegram Personalizer:** Strips out raw markdown constraints to deliver clean, highly scannable, mobile-optimized plain text blocks.
5. **Publishing Endpoints:** Pushes the finalized, uniquely styled updates directly live via native platform integrations.

---

## 🛠️ Tech Stack & Dependencies

* **Automation Engine:** Make.com (Formerly Integromat)
* **Large Language Model:** Google Gemini 2.5 Flash (via Google AI Studio)
* **Data Layer:** Google Sheets API
* **Publishing Frameworks:** LinkedIn API, Facebook Pages API, Telegram Bot API

---

## 📥 Getting Started & Deployment

Want to deploy this content machine for your own portfolio updates? Follow these steps:

### 1. Prerequisites
* A [Make.com](https://www.make.com/) account.
* A Google Gemini API Key from [Google AI Studio](https://aistudio.google.com/).
* Authorized connections for your target posting accounts (LinkedIn profile, Facebook Page, or Telegram Bot token).

### 2. Google Sheet Setup
Create a Google Sheet named `Automation content` with a column header in cell `A1` named exact text: `Content Links (A)`.

### 3. Importing the Blueprint
1. Download the `blueprint.json` file from this repository root directory.
2. Log into your Make.com dashboard, click **Create a new scenario**.
3. In the top-right options menu (three dots), click **Import Blueprint** and upload the file.
4. Click into each module node to map your localized app authorization tokens and Gemini API keys.
5. Flip the **Scheduling** toggle at the bottom-left corner to **ON**.

---

## 📝 Gemini Prompt Architecture

To bypass platform layout failures (such as raw markdown formatting code breaking social newsfeeds), each personalizer utilizes a explicit constraint engine:

> "STRICT RULES ON FORMATTING: Do not use any Markdown formatting characters under any circumstances. Never use asterisks (**) or underscores (_) to indicate bold or italic text. Output clean, plain text blocks only, using line breaks, capital letters, or emojis for emphasis instead."

---

## 👤 Developer Context

Built as a career-portfolio project demonstrating structural AI implementation, algorithmic routing pipelines, and multi-channel API provisioning.

* **GitHub:** [@PoojithaYelkur](https://github.com/PoojithaYelkur)
* **LinkedIn:** [@YelkurPoojitha](https://www.linkedin.com/in/yelkur-pujitha/)

Feel free to fork this blueprint repo, star it if you find it helpful, or open an issue if you want to optimize the parsing tracks!
