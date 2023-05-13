Note: This project is heavily work in progress and is not ready for production use.

# Textual

![Textual Logo](https://avatars.githubusercontent.com/u/133390985)

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

![Infrastructure Setup](https://myinfra.com/image)

- Cloudflare: The entrypoint for the application, proxies requests to the main server.
- VPC (AWS Virtual Private Cloud):
  - Main Server:
    - AppRunner: Hosts the NextJS application.
    - RDS (AWS Relational Database Service): Stores project-related data.
  - SQS (AWS Simple Queue Service): Stores tasks for the processing nodes.
  - Processing Nodes:
    - Node1, Node2, Node3: EC2 instances responsible for processing files.
- S3 (AWS Simple Storage Service): Stores the generated and user-uploaded files.

## Installation

To run the Textual project locally, follow these steps:

1. Clone the repository: `git clone https://github.com/your-username/textual.git`
2. Install project dependencies: `npm install`
3. Configure your AWS credentials and services according to the project's requirements.
4. Start the application: `npm start`

## Usage

Once the application is running, you can access it through your browser or API clients. Follow the provided documentation and guidelines to interact with the features and functionalities of the Textual application.

## Contribution

Contributions to the Textual project are welcome. If you encounter any issues or have suggestions for improvements, please open an issue on the project's GitHub repository.

## License

[MIT License](LICENSE)
