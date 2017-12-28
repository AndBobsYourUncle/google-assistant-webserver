# Instructions

## Thanks to Google for making this available
- https://github.com/googlesamples/assistant-sdk-python/tree/master/google-assistant-sdk
- https://developers.google.com/assistant/sdk/prototype/getting-started-other-platforms/config-dev-project-and-account

## Steps to use
* Create a Google account if you do not already have one
* Go to https://console.cloud.google.com/ to create a new project
* Go to API Management and activate the API Google Assistant and follow the given instructions (for the platform, use other). During the process, you will have to create an OAuth 2.0 ID in JSON, download this file
* Put that file inside this cloned repo's folder, with the filename `clientid.json`
* Build using Docker: `docker build -t andbobsyouruncle/google-assistant .`

If you need help, please use the links provided on top of this document.


## Run
`docker run -it -p 5000:5000 --name google-assistant andbobsyouruncle/google-assistant`

## Make broadcast requests
After the Docker container runs, you'll need to visit a link it gives you, and paste in the access code.

When that is finished, you should now be able to visit `http://localhost:5000/broadcast_message?message=YOUR MESSAGE HERE` to have Google Assistant broadcast your text message to all your Google Home speakers.
