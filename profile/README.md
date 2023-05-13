Note: This project is heavily work in progress and is not ready for production use.

# Textual

<p align="center">
  <a href="https://github.com/textual-org">
    <picture>
      <img src="https://avatars.githubusercontent.com/u/133390985" height="128">
    </picture>
  </a>
</p>

<p align="center">
  <a aria-label="Vercel logo" href="https://github.com/SGeri">
    <img src="https://img.shields.io/badge/SGeri-000000.svg?style=for-the-badge&labelColor=000">
  </a>
  <a aria-label="License" href="https://github.com/vercel/next.js/blob/canary/license.md">
    <img alt="" src="https://img.shields.io/npm/l/next.svg?style=for-the-badge&labelColor=000000">
  </a>
  <a aria-label="Web" href="https://github.com/textual-org/web-service">
    <img alt="" src="https://img.shields.io/badge/WEB-blueviolet.svg?style=for-the-badge&logo=Next.js&labelColor=000000&logoWidth=20">
  </a>
  <a aria-label="Processor" href="https://github.com/textual-org/processor">
    <img alt="" src="https://img.shields.io/badge/Python-blue.svg?style=for-the-badge&logo=Python&labelColor=000000&logoWidth=20">
  </a>
</p>

Textual is a medium-sized fullstack application that leverages OpenAI's Whisper trained models to generate speech recognized transcriptions for audio files. It aims to provide accurate and efficient transcription capabilities and has plans to support subtitle generation for movie sequences in the future.

## Technologies and Services Used

- AWS: Amazon Web Services, utilized for infrastructure needs.
- Cloudflare: Provides CDN and DDoS protection.
- OpenAI Whisper: Trained models for speech recognition.

- Postgres: Relational database for storing project-related data.

- NextJS: Full-stack typescript framework for the client and server code.
- Python: Runs the speech recognition and file processing code.

## Infrastructure Setup

The project's infrastructure is designed as follows:

![Infrastructure Setup](https://raw.githubusercontent.com/textual-org/.github/8d34c6d5bcc3806136e71f2ddc0d40b15285a63b/infrastructure.png)

- Cloudflare: The entrypoint for the application, proxies requests to the main server.
- VPC (AWS Virtual Private Cloud):
  - Main Server:
    - AppRunner: Hosts the NextJS application.
    - RDS (AWS Relational Database Service): Stores project-related data.
  - SQS (AWS Simple Queue Service): Stores tasks for the processing nodes.
  - Processing Nodes:
    - Node1, Node2, Node3: EC2 instances responsible for processing files.
- S3 (AWS Simple Storage Service): Stores the generated and user-uploaded files.

## Installation (TODO)

To run the Textual project locally, follow these steps:

1. Clone the repository: `git clone https://github.com/textual-org/textual.git`
2. Install project dependencies: `npm install`
3. Configure your AWS credentials and services according to the project's requirements.
4. Start the application: `npm start`

## Usage

Once the application is running, you can access it through your browser at our [website](https://to-be-done.com). Follow the provided documentation and guidelines to interact with the features and functionalities of the Textual application.

## Contribution

Contributions to the Textual project are welcome. If you encounter any issues or have suggestions for improvements, please open an issue on the project's GitHub repository.

## License

[MIT License](LICENSE)
