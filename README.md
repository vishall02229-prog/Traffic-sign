# Traffic Sign Classification — Streamlit

A Streamlit web app that uses the included `Traffic.h5` TensorFlow/Keras model to classify traffic-sign images into 43 classes.

## Project structure

```text
Traffic_Sign_Streamlit/
├── app.py
├── Traffic.h5
├── requirements.txt
├── README.md
├── .streamlit/
│   └── config.toml
└── test/
    ├── 1.png
    ├── 2.jpg
    ├── 3.png
    └── 4.jpg
```

## Run locally

```bash
pip install -r requirements.txt
streamlit run app.py
```

## Deploy on Streamlit Community Cloud

1. Create a new GitHub repository.
2. Upload the contents of this folder to the repository root.
3. Open Streamlit Community Cloud and create a new app.
4. Select your GitHub repository.
5. Set the main file to `app.py`.
6. Deploy.

The app loads `Traffic.h5` from the same folder as `app.py`.

## Model pipeline

Image → resize to 30×30 → normalize pixels to 0–1 → TensorFlow/Keras model → one of 43 traffic-sign classes.
