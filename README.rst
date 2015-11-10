This Fork is designed to work nicley with kranky (https://bitbucket.org/spikeCoder/kranky/overview), a lightweight python auditory stimulus presenter. It has two minor changes from the main open-ephys version ubuntu14.04:

1) Everytime the recording is started, a new data directory is created regardless of user input. This replaces the recording index in the default version.

2) The record control has some minor changes. 1) It takes a transient ttl pulse to either start or stop the recording rather than running recording as long as the record control channel is high. 2) It debounces the record control channel with a bounce time set in the code.  This stops the program from crashing if it gets record control signals too quickly.  


both the master and the ubuntu14.04 contain compiled versions of this version of open-ephys that run on ubtunu14.04 and 32 bit ubuntu12.10.  See GUI/Linux/build/open-ephys and GUI/Linux/build/open-ephys32

Jeff Knowles, UCSF (jeff.knowles@gmail.com)



==================================
Welcome to the Open Ephys project!
==================================

This GUI was designed to provide a fast and flexible interface for acquiring and visualizing data from extracellular electrodes.

Everything is written in C++, with the help of the Juce_ library. Juce is lightweight, easy to learn, and completely cross-platform. What's more, it includes a variety of classes for audio processing, which have been co-opted to process neural data. It might be necessary to create custom data processing classes in the future, but for now, Juce takes care of a lot of the messy bits involved in analyzing many parallel data streams.

This repository contains all of the files you'll need to compile and run the GUI on Linux, Mac OS X, and Windows. The makefile (for Linux), XCode project (for Mac), and Visual Studio 2012 project (Windows) are located in the Builds/ directory.

We recommend reading through the wiki_ before attempting to make any changes.

If you want to add files, you'll have to do that through the "Introjucer," using the "open-ephys.jucer" file. The Introjucer makefiles are located in the JuceLibraryCode/Introjucer/Builds folder, or as part of the Juce source_.

.. _source: https://github.com/julianstorer/juce
.. _JUCE: http://www.rawmaterialsoftware.com/juce.php
.. _wiki: http://open-ephys.atlassian.net
