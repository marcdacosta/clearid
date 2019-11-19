![exhibition-pic](/Users/m/repos/clearid/exhibition-pic.jpg)

# Clear ID

Has a doorman or cashier ever asked to see your ID? Have they used a device to scan it? Far from merely checking to see if the ID is valid, these products harvest some of our most personal data. Embedded in an ID’s barcode is all the information contained in the ID itself--our name, address, immigration status, binary gender, if we have poor eyesight or a prosthetic. The companies that sell ID scanning software are free to sell this data to third parties and provide analytics about the demographics and patterns of visitors to the establishments in their network. DMVs themselves have turned to our personal data as a source of revenue, often with [unsavory implications](https://www.vice.com/en_us/article/43kxzq/dmvs-selling-data-private-investigators-making-millions-of-dollars).

Clear ID is an installation that makes this dynamic visible by allowing participants to see what’s stored in their own personal barcodes. It asks what it would mean to return agency to people with respect to the identities they share and the ways they are reflected in corporate surveillance databases. After scanning their IDs, participants are invited to change their data and to print a new barcode in the same PDF417 standard used in “valid” IDs. 

Clear ID was first shown at the Mozilla-Tactical Tech [Glass Room Exhibition](https://theglassroom.org/san-francisco/exhibits) in October 2019 in San Francisco.



## ![barcode-printout](/Users/m/repos/clearid/barcode-printout.png)

## How the barcode works

The barcode on the reverse of a driver's license is encoded using the [PDF417](https://en.wikipedia.org/wiki/PDF417) standard. Anytime you see a barcode, it's just a graphical way of representing some text ([see more](https://simple.wikipedia.org/wiki/Barcode)). The [American Association of Motor Vehicle Administrators](https://www.aamva.org/) (AAMVA) sets a national standard for what data should be in the barcode and the standard way it should be formatted. In the image above, the `Barcode Contents` string of text is a direct representation of what is in the barcode above it. The AAMVA sets a standard for how that string of text should be formatted and how the field names are abbreviated. For a complete listing of embedded data fields see section `D.12.5.1 ` in the AAMVA DL/ID Card Design Standard (2016). 



## Some relevant libraries

- After using a scanner to read the barcode, it is straight forward to parse the string for the relevant fields ([reference implementation](https://github.com/abbasbeydoun/Python-PDF417-Driver-s-License-decoder/blob/master/decoder.py))
- [ihabunek/pdf417-py](ihabunek/pdf417-py) works well for making PDF417 barcodes out of any string of text