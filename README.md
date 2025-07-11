# HLR-lookup
## StarTrinity-Flask--Integration

This project contains a Python Flask server that interacts with the StarTrinity softswitch via CallXML. It supports:

- Real-time call answering logic
- Audio recording and background analysis (e.g. dead air, call center noise)
- IVR prompts and DTMF digit collection
- Honeypot filtering (e.g., early input detection, incorrect digit press)
- Dynamic XML generation

You must host the Flask app on the same server (or accessible from) where StarTrinity runs.

> 🔧 You will need to update your CallXML script to send HTTP requests to this Flask app for dynamic decisions.

A call is received on startinity softswitch that runs XML natively, the call header is forwards to the python flask that runs an HLR lookup on the  header payload from the XML(caller number).then forwards a response back to XML(startrinity softswitch) accepting or rejecting the call depending on the response.
