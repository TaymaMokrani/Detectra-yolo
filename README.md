# 🔥 Train YOLO Models Locally for Screen Activity Detection (Detectra Project)

**Author:** *Tayma Mokrani - Ilies Mraihi*  
**Last Updated:** 2025  
**Project:** Detectra – Real-Time Monitoring of Unauthorized Digital Activities

---

# 📌 Introduction

This notebook trains a **YOLO object detection model** using the Ultralytics library to detect **social media and AI tool usage directly from desktop screenshots**.

The trained model will become a core component of **Detectra**, a monitoring system that identifies distracting or unauthorized digital activities—such as visiting Facebook, Instagram, WhatsApp, Telegram, or ChatGPT—by analyzing what appears on a user’s screen in real time.

At the end of this notebook, you will have:

- ✅ A fully trained **YOLOv11m** model  
- ✅ Fine-tuned on your **custom screenshot dataset**  
- ✅ Able to detect multiple app windows inside a single screenshot  
- ✅ Ready for real-time integration:  
  - Detect → Take screenshot → Send to LLM → Notify supervisor

---

# 🎯 What This Notebook Covers

This notebook is optimized for **local training** on your computer.  
Your hardware:

- **GPU:** NVIDIA RTX 4050  
- **RAM:** 32 GB  
- **CPU:** Intel i7  

This environment allows you to train medium-to-large YOLO models quickly and efficiently.

You will:

1. Install Ultralytics  
2. Load your custom multi-class screenshot dataset  
3. Train a YOLOv8m model  
4. Validate the model  
5. Test predictions  
6. Export the final model  
7. Prepare for Detectra system integration  

---

# 📷 Dataset Description

Your dataset contains real desktop screenshots with multiple visible interfaces.  
Example classes include:

- `facebook`
- `instagram`
- `messenger`
- `whatsapp`
- `telegram`
- `chatgpt`
- `claude`
- `gemini`
- (Later: `X`, `youtube`, `tiktok`, etc.)

Because several apps can appear in the same image, your dataset uses **bounding boxes** (object detection), not classification.



