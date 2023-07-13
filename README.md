This repository contains Python scripts that automate text translation using AWS Translate and Google Cloud Translate services. The scripts can be run as standalone Python programs or deployed as AWS Lambda functions. There are two separate scripts included in the repository, each utilizing a different translation service.

## AWS Translation

The `translateAWS.py` script demonstrates how to translate text stored in an S3 object using AWS Translate. It uses the Boto3 library to interact with AWS services, specifically Amazon S3 and Amazon Translate. The translated text is then saved back to the S3 bucket for further use.

### Prerequisites

- Python 3.x
- Boto3 library
- AWS CLI configured with appropriate access and secret keys

### Usage

1. Configure AWS CLI with your AWS access and secret keys.
2. Customize the translation source and target languages by modifying the `lambda_handler` function in `aws_translation.py`.
3. Run the script either as a standalone Python program or deploy it as an AWS Lambda function triggered by S3 events.

## Google Cloud Translation

The `translateGCP.py` script demonstrates how to translate text extracted from a PDF file using the Google Cloud Translate API. It uses the `translate_v2` library from the `google.cloud` package to interact with the Google Cloud Translation service. The translated text is saved to an output file.

### Prerequisites

- Python 3.x
- `google-cloud-translate` library
- Google Cloud Translation API credentials

### Usage

1. Install the `google-cloud-translate` library using pip: `pip install google-cloud-translate`.
2. Obtain the Google Cloud Translation API credentials file in JSON format.
3. Customize the `pdf_filename`, `target_language`, and `output_filename` variables in `google_cloud_translation.py` according to your requirements.
4. Run the script as a standalone Python program.
