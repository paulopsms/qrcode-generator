<h1 align="center" style="font-weight: bold;">QR Code Generator 💻</h1>

![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Amazon S3](https://img.shields.io/badge/Amazon%20S3-FF9900?style=for-the-badge&logo=amazons3&logoColor=white)
![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)


<p align="center">
 <a href="#started">Getting Started</a> • 
  <a href="#routes">API Endpoints</a> •
 <a href="#future">Future Features</a>
</p>

<p align="center">
  <b>This is a simple service that has an endpoint to get a text and save as a QR Code in an Amazon S3 Bucket.</b>
</p>

<h2 id="started">🚀 Getting started</h2>

Here you describe how to run your project locally

<h3>Prerequisites</h3>

For this project to run, you'll need to have Docker and docker-compose installed.

- [Docker](https://docs.docker.com/engine/install)
- [Docker Compose](https://docs.docker.com/compose/install)

<h3>Cloning</h3>

How to clone your project

```bash
git clone https://github.com/paulopsms/qrcode-generator.git
```

<h3> Environment Variables</h2>

For the AWS S3Client work properly, you need to create your environment file `.env` your AWS credentials on it.

```yaml
AWS_REGION={BUCKET_REGION}
AWS_BUCKET_NAME={YOUR_BUCKET_NAME}
AWS_ACCESS_KEY_ID={YOUR_AWS_KEY_ID}
AWS_SECRET_ACCESS_KEY=YOUR_AWS_SECRET}
```

<h3>Starting</h3>

How to start your project.

Inside of your project folder, execute in your terminal:

```bash
docker comopose up -d --build
``````

<h2 id="routes">📍 API Endpoints</h2>

Here you can list the main routes of your API, and what are their expected request bodies.
​
| route               | description                                          
|----------------------|-----------------------------------------------------
| <kbd>POST /qrcode/generate</kbd>     | authenticate user into the api see [request details](#post-auth-detail)

<h3 id="post-auth-detail">POST /qrcode/generate</h3>

**REQUEST**
```json
{
  "text": "example"
}
```

**RESPONSE**
```json
{
    "url": "https://your-bucket-name.s3.your-region.amazonaws.com/random-uuid-generated"
}
```

<h2 id="future">🚀 Future Features</h2>

For the future of this project, there are two things I want to do:

1. Integrate to an URL Shortener that I'm developing.
2. Implement Redis Cache System.

