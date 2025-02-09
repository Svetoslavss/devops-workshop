<!DOCTYPE html>
<body>
  <h1>React with NodeJS Backend and MongoDB - CI/CD Pipeline</h1>
<p>
  <strong>
    <img src="https://upload.wikimedia.org/wikipedia/commons/a/a7/React-icon.svg" alt="React Logo" width="50" height="50">
    React
  </strong>
  with
  <strong>
    <img src="https://nodejs.org/static/images/logos/nodejs-new-pantone-black.svg" alt="NodeJS Logo" width="50" height="50">
    NodeJS
  </strong>
  Backend and
  <strong>
    <img src="https://www.mongodb.com/assets/images/global/leaf.svg" alt="MongoDB Logo" width="50" height="50">
    MongoDB
  </strong>
</p>

  <h2>About</h2>
  <p>
    This project is a <strong>React</strong> application that connects to a <strong>NodeJS backend</strong> and utilizes <strong>MongoDB</strong> for data storage. The application is designed to showcase a full-stack setup with frontend and backend components, along with a database.
  </p>
<p>
    The project is integrated with a <strong>CI/CD pipeline</strong> using 
    <strong>
        <img src="https://avatars.githubusercontent.com/u/44036562?s=200&v=4" 
             alt="GitHub Actions Logo" width="15" height="15"> GitHub Actions
    </strong>, allowing automated building, testing, and deployment of both the frontend and backend applications to 
    <strong>
        <img src="https://www.docker.com/wp-content/uploads/2022/03/Moby-logo.png" 
             alt="Docker Logo" width="15" height="15"> Docker Hub
    </strong>.
</p>

  <h2>Features</h2>
  <ul>
    <li><strong>Frontend</strong>: Developed using React.js, provides the user interface for interacting with the application.</li>
    <li><strong>Backend</strong>: Built using Node.js, handles API requests and communicates with the MongoDB database.</li>
    <li><strong>Database</strong>: MongoDB is used to store the application's data.</li>
    <li><strong>CI/CD Pipeline</strong>: Automatically builds and pushes Docker images for both frontend and backend applications to Docker Hub using GitHub Actions.</li>
  </ul>

  <h2>CI/CD Pipeline</h2>
  <p>This repository is equipped with a <strong>GitHub Actions</strong> CI/CD pipeline that automatically builds and deploys the frontend and backend Docker images whenever code is pushed to the <code>main</code> branch or a pull request is made to it.</p>

  <h3>CI/CD Workflow</h3>
  <ul>
    <li><strong>Triggers</strong>: The pipeline runs whenever a push or pull request is made to the <code>main</code> branch.</li>
    <li><strong>Steps</strong>:
      <ul>
        <li><strong>Build Frontend</strong>: The frontend React app is built and pushed to Docker Hub with the tag <code>frontend:latest</code>.</li>
        <li><strong>Build Backend</strong>: After the frontend build completes, the backend Node.js app is built and pushed to Docker Hub with the tag <code>backend:latest</code>.</li>
      </ul>
    </li>
  </ul>
  <p>The CI/CD workflow uses <strong>Docker</strong>, <strong>QEMU</strong>, and <strong>Docker Buildx</strong> to handle the building and pushing of Docker images.</p>

  <h2>Technologies Used</h2>
  <ul>
    <li><strong>Frontend</strong>: React.js</li>
    <li><strong>Backend</strong>: Node.js</li>
    <li><strong>Database</strong>: MongoDB</li>
    <li><strong>CI/CD</strong>: GitHub Actions, Docker</li>
    <li><strong>Containerization</strong>: Docker</li>
  </ul>

  <h2>Setting Up the Project Locally</h2>
  <h3>1. Clone the repository</h3>
  <pre><code>git clone https://github.com/yourusername/your-repository.git
cd your-repository</code></pre>

  <h3>2. Install Dependencies</h3>
  <p><strong>Frontend:</strong></p>
  <pre><code>cd frontend
npm install</code></pre>
  <p><strong>Backend:</strong></p>
  <pre><code>cd backend
npm install</code></pre>

  <h3>3. Set Up MongoDB</h3>
  <p>Ensure MongoDB is running locally or configure your backend to connect to a remote MongoDB service.</p>

  <h3>4. Running the Application</h3>
  <p><strong>Frontend:</strong></p>
  <pre><code>cd frontend
npm start</code></pre>
  <p><strong>Backend:</strong></p>
  <pre><code>cd backend
npm start</code></pre>
  <p>The application will be running at <code>http://localhost:3000</code> for the frontend and the backend API will be available at <code>http://localhost:5000</code>.</p>

  <h2>Docker Setup</h2>
  <p>Both the frontend and backend applications have their respective Dockerfiles located in the <code>./frontend/Dockerfile</code> and <code>./backend/Dockerfile</code> directories. These files are used in the CI/CD pipeline to build Docker images for both components.</p>
  <p>To build and run the application using Docker locally:</p>
  <h3>1. Frontend</h3>
  <pre><code>docker build -t frontend:latest ./frontend
docker run -p 3000:3000 frontend:latest</code></pre>
  <h3>2. Backend</h3>
  <pre><code>docker build -t backend:latest ./backend
docker run -p 5000:5000 backend:latest</code></pre>

  <h2>Docker Hub</h2>
  <p>After the CI/CD pipeline runs, the latest images will be pushed to <strong>Docker Hub</strong> with the tags:</p>
  <ul>
    <li><code>frontend:latest</code></li>
    <li><code>backend:latest</code></li>
  </ul>
  <p>You can access the images directly from Docker Hub:</p>
  <ul>
    <li><a href="https://hub.docker.com/r/svetoslavds/frontend" target="_blank">Frontend Docker Hub Repository</a></li>
    <li><a href="https://hub.docker.com/r/svetoslavds/backend" target="_blank">Backend Docker Hub Repository</a></li>
  </ul>

  <h2>Contributing</h2>
  <p>Contributions are welcome! Please fork this repository, create a new branch for your changes, and submit a pull request.</p>

  <h2>License</h2>
  <p>This project is licensed under the MIT License - see the <a href="LICENSE" target="_blank">LICENSE</a> file for details.</p>

</body>
</html>
