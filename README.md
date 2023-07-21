<center><img src="https://raw.githubusercontent.com/xnl-h4ck3r/GAP-Burp-Extension/main/GAP/images/title.png"></center>

## About - v3.5

This is an evolution of the original getAllParams extension for Burp. Not only does it find more potential parameters for you to investigate, but it also finds potential links to try these parameters on, and produces a target specific wordlist to use for fuzzing.
The full Help documentation can be found [here](https://github.com/xnl-h4ck3r/burp-extensions/blob/main/GAP%20Help.md) or from the Help icon on the GAP tab.

## TL;DR

### Installation

1. Visit [Jython Offical Site](https://www.jython.org/download), and download the latest stand alone JAR file, e.g. `jython-standalone-2.7.3.jar`.
2. Open Burp, go to **Extensions** -> **Extension Settings** -> **Python Environment**, set the **Location of Jython standalone JAR file** and **Folder for loading modules** to the directory where the Jython JAR file was saved.
3. On a command line, go to the directory where the jar file is and run `java -jar jython-standalone-2.7.3.jar -m ensurepip`.
4. Download the `GAP.py` and `requirements.txt` from this project and place in the same directory.
5. Install Jython modules by running `java -jar jython-standalone-2.7.3.jar -m pip install -r requirements.txt`.
6. Go to the **Extensions** -> **Installed** and click **Add** under **Burp Extensions**.
7. Select **Extension type** of **Python** and select the **GAP.py** file.

### Using

1. Just select a target in your Burp scope (or multiple targets), or even just one subfolder or endpoint, and choose extension **GAP**:

<center><img src="https://raw.githubusercontent.com/xnl-h4ck3r/GAP-Burp-Extension/main/GAP/images/run.png"></center>

Or you can right click a request or response in any other context and select **GAP** from the **Extensions** menu.

2. Then go to the **GAP** tab to see the results:

<center><img src="https://raw.githubusercontent.com/xnl-h4ck3r/GAP-Burp-Extension/main/GAP/images/tab.png"></center>

## Notes

If you don't need one of the modes, then un-check it as results will be quicker.
The Words mode uses the `beautifulsoup4` library and this can be quite slow, so be patient!

## In Depth Instructions

Below is an in-depth look at the GAP Burp extension, from installing it successfully to explaining all of the features.
<b>NOTE: This video is from 16th July 2023 and explores v3.X, so any features added after this may not be featured</b><br>

<center><iframe width="560" height="315" src="https://www.youtube.com/embed/Os3bN0zUROA?si=KKr9YWFiA40YD1N_" title="GAP Burp Extension" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe><center>

## TODO

- Improve the performance of writing the output files. For some reason this can take a looooong time in some cases.
- Use an alternative to `beautifulsoup4` that is faster to parse responses for Words.

Good luck and good hunting!
If you really love the tool (or any others), or they helped you find an awesome bounty, consider [BUYING ME A COFFEE!](https://ko-fi.com/xnlh4ck3r) ☕ (I could use the caffeine!)

🤘 /XNL-h4ck3r

<a href='https://ko-fi.com/B0B3CZKR5' target='_blank'><img height='36' style='border:0px;height:36px;' src='https://storage.ko-fi.com/cdn/kofi2.png?v=3' border='0' alt='Buy Me a Coffee at ko-fi.com' /></a>
