# Climate-Cast

**Climate-Cast** is a fast and modern weather app built using **React**, **Vite**, and **Tailwind CSS**. It allows users to search for real-time weather data by city and displays results in a clean, responsive UI.

---

## 🚀 Features

- 🔍 Search weather by city name
- 🌡️ View temperature, humidity, wind, etc.
- ⚡ Super-fast performance with Vite
- 🎨 Responsive Tailwind CSS styling
- 📱 Mobile-friendly UI

---

## 🛠️ Tech Stack

- **Frontend**: React, Vite, Tailwind CSS
- **Weather API**: OpenWeatherMap
- **Deployment**: Docker, Kubernetes, Jenkins

---

## Local Development

1. Clone the Repository

```
git clone https://github.com/yourusername/climate-cast.git
cd climate-cast
npm install
```

2. Create .env

```
VITE_WEATHER_API_KEY=your_api_key_here
```

3. Run the App Locally

```
npm run dev

visit : http://localhost:5173
```


## 🐳 Docker Deployment

1. Build Image

```
docker build -t climate-cast-image .
```

2. Run Application
```
docker run -d --name climate-app -p 5000:5173 climate-cast-image:latest
```

## ☸️ Kubernetes Deployment (On Kind Cluster)

1. Push Image to DockerHub

```
docker build -t your_dockerhub/climate-cast .
docker push your_dockerhub/climate-cast
```

2. Go to **Kubernetes** Directory and Run the all manifest files

```
kubectl apply -f .
```

3. Port Forwarding

```
kubectl port-forward svc/<service-name> -n namespace -p 5000:5173 --address=0.0.0.0
```

4. Visit
```
http://localhost:5000
```


## 🔁 Jenkins CI/CD Pipeline


Go to **Jenkinsfile**