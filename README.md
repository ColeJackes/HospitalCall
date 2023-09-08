# HospitalCall
Project to allow users to call into a number, provide healthcare data and choose an appointment time.

To run locally:

1. populate .env file with all the API keys listed in .env.template
2. run Redis locally on port 6379
3. ngrok http 3000
4. copy ngrok URL to .env file (not including https://)
5. copy ngrok URL to Twilio configuration settings with /inbound_call at the end, and including https:// at the beginning
6. activate the virtual env
7. uvicorn receive_calls:app --reload --port 3000
8. call the corresponding phone number to test!
