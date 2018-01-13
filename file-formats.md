# File Formats

Below described are the file formats used for modding. and methods to convert, extract and repack files.

### Fast Files

> Extension: .ff

Fast Files are file containers. Maps and Mods are packed in this format. Some unpacking and repacking tools do exist. The [fast file unpacker by Tom Crowley](http://tom-crowley.co.uk/downloads/) works well for unpacking gsc scripts.

### IWD Files

> Extension: .iwd

Another container file format. IWD files are simply ZIP files and can be opened and written with any program understanding the ZIP file format. [7-zip](http://www.7-zip.de/) is a good choice to edit IWD files because it lets you directly edit contained files.

### GSC Files

> Extension: .gsc

Text files containing server side scripting code. As GSC syntax is quite similar to C, syntax highlighting more or less works in all editors. The best known solution currently is using [Visual Studio Code](https://code.visualstudio.com/) with the [CoD-Sense plugin](https://marketplace.visualstudio.com/items?itemName=se2dev.cod-sense), which provides syntax highlighting explicitely for GSC code.

### CFG Files

> Extension: .cfg

Textfiles containing server commands line by line.

