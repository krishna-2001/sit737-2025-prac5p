
---

## 🛠️ Steps Taken

### 1️⃣ Setup the Application

- Created a simple application (e.g., a Node.js web server).
- Placed the code in the `app/` directory.
- Ensured it listens on port 3000 and responds with basic text or JSON.

### 2️⃣ Created Dockerfile

- Created a `Dockerfile` in the root directory to define the image build process.
- The Dockerfile includes:
  - Base image (e.g., `node:18-alpine`)
  - Copying of source code
  - Installation of dependencies
  - Port exposure and default start command

**Sample Dockerfile:**
```Dockerfile
FROM node:18-alpine
WORKDIR /app
COPY app/ .
RUN npm install
EXPOSE 3000
CMD ["node", "index.js"]
