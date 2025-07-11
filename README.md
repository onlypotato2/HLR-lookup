# HLR-lookup
A call is received on startinity softswitch that runs XML natively, the call header is forwards to the python flask that runs an HLR lookup on the  header payload from the XML(caller number).then forwards a response back to XML(startrinity softswitch) accepting or rejecting the call depending on the response.
