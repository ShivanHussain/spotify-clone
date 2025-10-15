# 🎵 Spotify Clone

A responsive web application that replicates the core features of Spotify's web player interface. Built using HTML, CSS, and JavaScript, this project demonstrates frontend development skills and the ability to mimic popular UI designs.

##  Features

- **Responsive Design**: Optimized for both desktop and mobile views.
- **Spotify-Inspired UI**: Mimics Spotify's layout, including sidebar navigation, music cards, and playback controls.
- **CSS Styling**: Utilizes custom CSS for layout and design, with icons from Font Awesome.
- **Docker Support**: Includes Dockerfile and docker-compose.yml for containerization.

##  Technologies Used

- **HTML5**: Structure and semantics.
- **CSS3**: Styling and layout.
- **JavaScript**: Interactive elements (if applicable).
- **Docker**: Containerization for easy deployment.

##  Installation

### Clone the Repository

```bash
git clone https://github.com/ShivanHussain/spotify-clone.git
cd spotify-clone
```

### Run Locally

1. **Without Docker**:
   - Open `index.html` in your preferred web browser.

2. **With Docker**:
   - Build and run the Docker container:

   ```bash
   docker-compose up --build
   ```

   - Access the application at `http://localhost:3000`.

## 🧪 Testing

To ensure the application functions correctly:

1. **Manual Testing**:
   - Open the application in a browser.
   - Verify that all UI components are responsive and interactive.

2. **Automated Testing** (if applicable):
   - Implement JavaScript testing using frameworks like Jest or Mocha.

## 🚢 Deployment

For deployment on a server:

1. **Build the Docker Image**:

   ```bash
   docker build -t spotify-clone .
   ```

2. **Run the Docker Container**:

   ```bash
   docker run -d -p 3000:80 spotify-clone
   ```

3. **Access the Application**:
   - Navigate to `http://your-server-ip:3000` in a web browser.

## ⚙️ Configuration

- **Dockerfile**: Defines the environment and build steps for the application.
- **docker-compose.yml**: Simplifies the process of building and running the Docker container.
