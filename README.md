# Desi-Scribe: AI-Powered Advertisement Poster Generator

An AI-powered advertisement poster generator that transforms product information into production-ready marketing creatives using Qwen, BLIP, and Stable Diffusion XL.

## 🚀 Overview

**Desi-Scribe** is an AI-powered creative generation system designed to automate the process of creating advertisement posters from simple product information.

The system combines multiple generative AI models to understand products, generate marketing content, create visual assets, and compose them into a final advertisement poster.

### Key Capabilities

- 🧠 Product understanding using **Qwen**
- ✍️ AI-generated marketing copy
- 🎨 Image generation using **Stable Diffusion XL**
- 👁️ Image understanding using **BLIP**
- 🖼️ Automated advertisement poster composition
- ⚡ Optimized AI inference pipeline
- 🌍 Multilingual content generation
- 🚀 Production-ready creative generation in approximately **3–6 seconds**

---

## 🛠️ Tech Stack

| Category | Technologies |
|---|---|
| Language | Python |
| Backend | FastAPI, Flask |
| LLM | Qwen |
| Image Generation | Stable Diffusion XL |
| Image Understanding | BLIP |
| Deep Learning | PyTorch |
| Frontend | HTML, CSS, JavaScript |
| AI Frameworks | Hugging Face Transformers, Diffusers |
| API | REST API |

---

## 🧠 AI Pipeline

The application uses three major AI components:

### 1. Qwen — Product Understanding

Qwen analyzes the provided product information and extracts useful marketing information such as:

- Product name
- Product category
- Product features
- Product benefits
- Target audience
- Marketing keywords
- Promotional messaging
- Visual requirements

### 2. Stable Diffusion XL — Visual Generation

Stable Diffusion XL generates high-quality visual assets based on AI-generated prompts.

It can create:

- Product backgrounds
- Lifestyle scenes
- Promotional visuals
- Creative compositions
- Marketing imagery

### 3. BLIP — Image Understanding

BLIP analyzes images and generates useful visual descriptions.

It can be used for:

- Image captioning
- Visual understanding
- Object/context analysis
- Improving generated advertisement content

---

## 🔄 Workflow

```text
                 Product Information
                         │
                         ▼
                ┌─────────────────┐
                │     Qwen LLM    │
                │ Product Analysis│
                └────────┬────────┘
                         │
                         ▼
                Marketing Copy
                & Visual Prompt
                         │
                         ▼
              ┌─────────────────────┐
              │ Stable Diffusion XL │
              │   Image Generation  │
              └──────────┬──────────┘
                         │
                         ▼
                  Generated Visual
                         │
                         ▼
                 ┌──────────────┐
                 │     BLIP     │
                 │Image Analysis│
                 └──────┬───────┘
                        │
                        ▼
              ┌───────────────────┐
              │ Poster Composition│
              └─────────┬─────────┘
                        │
                        ▼
                Final Advertisement
```

---

## 📋 Example

### Input

```text
Product Name:
Premium Wireless Headphones

Description:
Noise-cancelling wireless headphones with
40-hour battery life and premium sound quality.

Brand:
SoundX
```

### AI Processing

The system analyzes the product and generates:

```text
Target Audience:
Music enthusiasts and professionals

Key Features:
- Active Noise Cancellation
- 40-hour battery
- Premium audio quality

Marketing Headline:
Experience Sound Without Limits

Call To Action:
Shop Now
```

The generated information is then used to create a visual prompt for Stable Diffusion XL.

### Output

The final output is a complete advertisement poster containing:

- AI-generated visuals
- Marketing headline
- Product information
- Key features
- Brand information
- Call-to-action
- Professional layout

---

## ⚡ Performance

The inference pipeline is optimized to reduce unnecessary computation and improve end-to-end generation speed.

### Target Generation Time

```text
Approximately 3–6 seconds
```

Actual performance may vary depending on:

- GPU hardware
- Image resolution
- Number of inference steps
- Model configuration
- Model loading strategy
- Concurrent requests

---

## 🌍 Multilingual Support

The system is designed to support multilingual advertisement generation.

Example languages include:

```text
English
Hindi
Spanish
French
German
```

Users can specify the desired language while generating the advertisement.

---

## 🎯 Use Cases

Desi-Scribe can be used for generating marketing creatives for:

- 🛒 E-commerce products
- 👟 Fashion brands
- 📱 Consumer electronics
- 🍔 Food and beverage
- 💄 Beauty and cosmetics
- 🏠 Real estate
- 🚗 Automotive
- 🏋️ Fitness products
- 📢 Social media campaigns
- 🏷️ Promotional campaigns

---

## 🏗️ Project Architecture

```text
User
 │
 ▼
Frontend
 │
 ▼
FastAPI / Flask
 │
 ▼
AI Orchestrator
 │
 ├───────────────┐
 ▼               ▼
Qwen            BLIP
 │               │
 ▼               │
Marketing        │
Content          │
 │               │
 └───────┬───────┘
         │
         ▼
Stable Diffusion XL
         │
         ▼
Generated Visual
         │
         ▼
Poster Composer
         │
         ▼
Final Advertisement
```

---

## 📂 Project Structure

```text
Desi-Scribe-AI-Powered-Advertisement-Poster-Generator/
│
├── app/
│   ├── main.py
│   │
│   ├── routes/
│   │   ├── generate.py
│   │   └── health.py
│   │
│   ├── models/
│   │   ├── qwen.py
│   │   ├── blip.py
│   │   └── sdxl.py
│   │
│   ├── pipeline/
│   │   ├── orchestrator.py
│   │   ├── prompts.py
│   │   └── composer.py
│   │
│   └── utils/
│       ├── image_utils.py
│       └── text_utils.py
│
├── frontend/
│   ├── index.html
│   ├── style.css
│   └── script.js
│
├── outputs/
│
├── requirements.txt
├── .env.example
├── .gitignore
└── README.md
```

---

## 💻 Installation

### Prerequisites

Make sure you have the following installed:

- Python 3.9+
- pip
- Git
- CUDA-enabled GPU recommended

### Clone the Repository

```bash
git clone https://github.com/agrawalayush29/Desi-Scribe-AI-Powered-Advertisement-Poster-Generator.git
```

```bash
cd Desi-Scribe-AI-Powered-Advertisement-Poster-Generator
```

### Create Virtual Environment

#### Windows

```bash
python -m venv venv
```

```bash
venv\Scripts\activate
```

#### Linux / macOS

```bash
python3 -m venv venv
```

```bash
source venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

## ⚙️ Environment Configuration

Create a `.env` file in the root directory:

```env
MODEL_DEVICE=cuda

QWEN_MODEL=Qwen/Qwen2.5-7B-Instruct
SDXL_MODEL=stabilityai/stable-diffusion-xl-base-1.0
BLIP_MODEL=Salesforce/blip-image-captioning-base

OUTPUT_DIR=outputs
```

For CPU inference:

```env
MODEL_DEVICE=cpu
```

> GPU inference is recommended for faster image generation.

---

## ▶️ Running the Application

Start the backend:

```bash
python app/main.py
```

Or run using Uvicorn:

```bash
uvicorn app.main:app --reload
```

The API will be available at:

```text
http://localhost:8000
```

Open the frontend in your browser to start generating advertisement posters.

---

## 🔌 API Usage

### Generate Advertisement

```http
POST /generate
Content-Type: application/json
```

### Request

```json
{
  "product_name": "Premium Wireless Headphones",
  "description": "Noise cancelling headphones with 40-hour battery life",
  "brand": "SoundX",
  "language": "English"
}
```

### Response

```json
{
  "status": "success",
  "message": "Poster generated successfully",
  "output": "outputs/generated_poster.png"
}
```

---

## 🔐 Security

Never commit API keys, access tokens, or other sensitive credentials to GitHub.

Use environment variables instead:

Add the following to `.gitignore`:

```gitignore
.env
venv/
__pycache__/
*.pyc
outputs/*
```

---

## 📈 Traditional vs AI-Powered Workflow

### Traditional Process

```text
Product Information
        ↓
Copywriter
        ↓
Graphic Designer
        ↓
Image Search / Creation
        ↓
Manual Editing
        ↓
Final Advertisement
```

### Desi-Scribe Process

```text
Product Information
        ↓
       AI
        ↓
Product Understanding
        ↓
Marketing Copy
        ↓
Visual Generation
        ↓
Poster Composition
        ↓
Final Advertisement
```

This reduces the amount of manual effort required to create marketing creatives.

---

## 🔮 Future Improvements

- [ ] Custom brand templates
- [ ] Automatic logo placement
- [ ] Multiple poster layouts
- [ ] Social media-specific templates
- [ ] Instagram post generation
- [ ] Instagram story generation
- [ ] LinkedIn advertisement generation
- [ ] YouTube thumbnail generation
- [ ] Batch poster generation
- [ ] User authentication
- [ ] Poster history
- [ ] Download functionality
- [ ] Docker deployment
- [ ] Cloud deployment
- [ ] GPU optimization
- [ ] Model quantization
- [ ] Advanced typography generation
- [ ] Custom brand style support

---

## 📊 Project Highlights

| Feature | Details |
|---|---|
| Product Understanding | Qwen |
| Image Understanding | BLIP |
| Image Generation | Stable Diffusion XL |
| Backend | FastAPI / Flask |
| Frontend | HTML / CSS / JavaScript |
| Generation Time | ~3–6 seconds |
| Language Support | Multilingual |
| Output | Advertisement Posters |

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the repository
2. Create a new branch

```bash
git checkout -b feature/new-feature
```

3. Make your changes
4. Commit your changes

```bash
git commit -m "Add new feature"
```

5. Push the branch

```bash
git push origin feature/new-feature
```

6. Open a Pull Request

---

## 📜 License

This project is intended for educational, research, and development purposes.

Add an appropriate license based on the models and libraries used in this project.

---

## 👨‍💻 Author

**Ayush Agrawal**

AI / ML Developer

GitHub: `https://github.com/agrawalayush29`

LinkedIn: `https://www.linkedin.com/in/ayush-agrawal-1825582a0`

---

## ⭐ Support

If you found this project useful, please consider giving the repository a ⭐.

---

## 📌 Project Summary

**Desi-Scribe** is an AI-powered advertisement generation platform that combines **Qwen for product understanding, BLIP for image understanding, and Stable Diffusion XL for visual generation**. The optimized FastAPI/Flask pipeline transforms simple product information into production-ready marketing creatives within seconds.
