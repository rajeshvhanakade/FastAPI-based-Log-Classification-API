<h1>📊 Log Classification API</h1>

<p>
A RESTful API built using <strong>FastAPI</strong> for automated log classification.  
The system accepts a CSV file containing log sources and messages, applies a machine learning or rule-based classifier,
and returns a new CSV file with predicted target labels.
</p>

<div class="section">
    <span class="badge">Python</span>
    <span class="badge">FastAPI</span>
    <span class="badge">Pandas</span>
    <span class="badge">ML Classification</span>
    <span class="badge">REST API</span>
</div>

<hr>

<div class="section">
<h2>🚀 Features</h2>
<ul>
    <li>📁 Upload CSV file for batch log classification</li>
    <li>🧠 Automatic log categorization using a classifier</li>
    <li>📤 Returns classified CSV file as output</li>
    <li>⚡ High-performance FastAPI backend</li>
    <li>🧪 Built-in validation for input schema</li>
    <li>🔐 Error handling for invalid files and formats</li>
</ul>
</div>

<hr>

<div class="section">
<h2>🧠 System Workflow</h2>

<pre>
Client Uploads CSV
        │
        ▼
FastAPI Endpoint (/classify)
        │
        ▼
Pandas DataFrame Loader
        │
        ▼
Log Classifier (classify.py)
        │
        ▼
Append Target Label Column
        │
        ▼
Return Output CSV
</pre>

</div>

<hr>

<div class="section">
<h2>📁 Project Structure</h2>

<pre>
log-classification-api/
│
├── main.py              # FastAPI application
├── classify.py          # Log classification logic
├── resources/
│   └── output.csv       # Generated classified output
├── requirements.txt
└── README.html
</pre>

</div>

<hr>

<div class="section">
<h2>⚙️ Installation</h2>

<h3>1️⃣ Clone Repository</h3>
<pre>
git clone https://github.com/your-username/log-classification-api.git
cd log-classification-api
</pre>

<h3>2️⃣ Create Virtual Environment</h3>
<pre>
python -m venv venv
source venv/bin/activate   (Linux/Mac)
venv\Scripts\activate      (Windows)
</pre>

<h3>3️⃣ Install Dependencies</h3>
<pre>
pip install -r requirements.txt
</pre>
</div>

<hr>

<div class="section">
<h2>▶️ Run the API Server</h2>

<pre>
uvicorn main:app --reload
</pre>

<p>
Server will start at:
</p>

<pre>
http://127.0.0.1:8000
</pre>

</div>

<hr>

<div class="section">
<h2>📤 API Usage</h2>

<h3>Endpoint</h3>
<pre>
POST /classify/
</pre>

<h3>Input CSV Format</h3>
<pre>
source,log_message
auth_service,User login failed
db_service,Connection timeout
</pre>

<h3>Response</h3>
<p>
Returns a CSV file with an additional column:
</p>

<pre>
source,log_message,target_label
auth_service,User login failed,Authentication Error
db_service,Connection timeout,Database Error
</pre>

</div>

<hr>

<div class="section">
<h2>🛠 Technology Stack</h2>
<ul>
    <li>Python</li>
    <li>FastAPI</li>
    <li>Pandas</li>
    <li>Uvicorn</li>
    <li>Custom classification module</li>
</ul>
</div>

<hr>

<div class="section">
<h2>🔐 Input Validation</h2>
<ul>
    <li>Only CSV files are accepted</li>
    <li>Required columns: <code>source</code>, <code>log_message</code></li>
    <li>Returns HTTP 400 for invalid file format</li>
    <li>Returns HTTP 500 for server-side errors</li>
</ul>
</div>

<div class="section">
<h2>📜 License</h2>
<p>
This project is licensed under the MIT License.
</p>
</div>

<hr>


</body>
</html>
