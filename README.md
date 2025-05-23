<h1>🚨 Sentiment Analysis Pungli - Indonesia Case Study 🇮🇩</h1>

<p>Proyek ini merupakan implementasi <strong>Natural Language Processing (NLP)</strong> untuk melakukan analisis sentimen terhadap laporan praktik pungutan liar (pungli) masyarakat Indonesia. Model ini mengklasifikasikan opini ke dalam 3 sentimen:</p>

<ul>
  <li><code>0</code>: Netral</li>
  <li><code>1</code>: Positif</li>
  <li><code>2</code>: Negatif</li>
</ul>

<h2>📁 Dataset</h2>
<p>Dataset berasal dari kumpulan opini atau review masyarakat mengenai pungli. Dataset disimpan dalam file. Source: https://www.google.com/maps/place/Gn.+Pancar/@-6.5916664,106.9016446,15z/data=!3m1!4b1!4m6!3m5!1s0x2e69c78788c45c61:0xa3a314728543d7f5!8m2!3d-6.5916667!4d106.9119444!16s%2Fg%2F113qbs8nv?hl=id&entry=ttu&g_ep=EgoyMDI1MDQzMC4xIKXMDSoASAFQAw%3D%3D <code>pungli.csv</code>.</p>

<h2>⚙️ Preprocessing</h2>
<p>Langkah-langkah pembersihan data teks dilakukan sebagai berikut:</p>
<ol>
  <li>Clean karakter non-alfanumerik</li>
  <li>Lowercasing</li>
  <li>Stopword removal (custom stopword)</li>
  <li>Stemming menggunakan <strong>Sastrawi</strong></li>
  <li>Tokenization dan padding</li>
</ol>

<h2>🧠 Model</h2>
<p>Model yang digunakan adalah <strong>LSTM (Long Short-Term Memory)</strong> dengan arsitektur:</p>
<ul>
  <li>Embedding Layer (128 dimensi)</li>
  <li>Dense Layer (128 dan 256)</li>
  <li>SpatialDropout1D (0.2)</li>
  <li>LSTM Layer (128 unit, dropout)</li>
  <li>Dropout Layer (0.5)</li>
  <li>Output: Dense(3) + Softmax</li>
</ul>

<p><strong>Optimizer:</strong> Adam<br>
<strong>Loss:</strong> sparse_categorical_crossentropy<br>
<strong>Epochs:</strong> 50</p>

<h2>📊 Deep Analysis</h2>
<p>Analisis mendalam dilakukan untuk memahami persebaran sentimen:</p>
<ul>
  <li>Distribusi sentimen</li>
  <li>Wordcloud untuk tiap sentimen</li>
  <li>Confusion matrix</li>
  <li>Classification report</li>
  <li>Insight visual dalam bentuk grafik</li>
</ul>

<h2>🖼️ Contoh Visualisasi</h2>
<img src="images/download (36).png" width="45%" style="margin-right:10px;" />
<img src="images/download (37).png" width="45%" />

<h2>🧪 Contoh Prediksi</h2>
<pre><code>Input  : tempatnya agak kurang, banyak pungli dimana mana
Output : Predicted Sentiment: 2 (Negatif)</code></pre>

<h2>🛠️ Tools & Libraries</h2>
<ul>
  <li>Pandas, NumPy</li>
  <li>NLTK, Sastrawi</li>
  <li>TensorFlow / Keras</li>
  <li>Matplotlib, Seaborn</li>
  <li>WordCloud</li>
</ul>

<h2>💾 File Penting</h2>
<ul>
  <li><code>pungli.csv</code> – Dataset</li>
  <li><code>modaljalan4.h5</code> – Model hasil training</li>
  <li><code>combined2.txt</code> – Model versi TFLite</li>
</ul>

<h2>📥 Cara Menjalankan</h2>
<pre><code>pip install -r requirements.txt
python model_training.py
python deep_analysis.py
</code></pre>

<h2>👨‍💻 Author</h2>
<p><strong>Faiq</strong> – Teknik Informatika, fokus di bidang Data Science dan NLP</p>
