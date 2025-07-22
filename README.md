
# 🔍 Image Search with CLIP (Contrastive Language–Image Pretraining)

This project allows you to **search images using natural language queries** by leveraging the power of OpenAI's **CLIP** model. It loads a folder of images, generates embeddings, and then finds the most similar images to your text description.

Built for use in **Google Colab** or local Python environments.

---

## 🧠 Powered by CLIP

CLIP (Contrastive Language–Image Pretraining) is a powerful vision-language model that understands both images and text. This project uses CLIP to extract image embeddings and compare them with text queries using cosine similarity.

---

## 🗂️ Project Workflow

1. **Load CLIP Model**  
   Loads `openai/clip-vit-base-patch32` via 🤗 Hugging Face.

2. **Load Images**  
   Scans the `images/` directory and loads `.jpg` files.

3. **Extract Embeddings**  
   Images are processed and converted into feature vectors.

4. **Search**  
   User types a natural language query. Top-3 most similar images are returned with similarity scores.

---

## 🖼️ Sample Output

```

Loading CLIP model and processor...
CLIP model loaded successfully!

Loading images from 'images'...
Loaded: 310715139\_7f05468042.jpg
Loaded: 311619377\_2ba3b36675.jpg
...

Extracting image features (embeddings)... This might take a moment.
Image features extracted.

Enter your search query (e.g., 'a cat in a garden', 'a fast car', or 'exit' to quit): image with black dog

Top 3 results for 'image with black dog':

* images/333973142\_abcd151002.jpg (Similarity: 0.2749)
* images/326456451\_effadbbe49.jpg (Similarity: 0.2684)
* images/3101796900\_59c15e0edc.jpg (Similarity: 0.2520)

````

---

## 🔧 Requirements

Install dependencies with:

```bash
pip install torch torchvision torchaudio
pip install transformers
pip install pillow
````

---

## 📁 Folder Structure

```
project/
│
├── main.py               # Main search script
├── images/               # Folder containing all images
│   ├── image1.jpg
│   ├── image2.jpg
│   └── ...
└── README.md
```

---

## ▶️ How to Use

1. Clone the repo or upload your images to a folder named `images/`.
2. Run the script and wait for embeddings to be generated.
3. Type any **text prompt** (like "a dog on grass") and view the results.
4. Type `'exit'` to quit the loop.

---

## 💬 Example Queries

* "a man riding a bicycle"
* "a dog laying on the ground"
* "a child playing with a toy"
* "a group of people walking"

---

## 📄 License

This project is for educational and research purposes only.
CLIP is provided under the license of OpenAI and Hugging Face.

---

