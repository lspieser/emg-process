# Example code to process EMG signal and EMG burst onsets and offsets using myonset.

Myonset is a python package to process and detect signal burst(s) onset and offset, especially developed for electromyographic (EMG) signal. 
Myonset implements tools for signal preprocessing, automatic onset and offset detection, as well as vizualisation and correction of onset and offset latencies.
Jupyter notebooks containing simple example code to process EMG signal and detect EMG burst onsets and offets can be found in [tutorials](https://github.com/lspieser/myonset/tree/main/tutorials) on [myonset repository] (https://github.com/lspieser/myonset/tree/main).
This repository contains more complete example code that we use in our laboratory to process EMG data in experimental psychology tasks (mostly choice reaction-time tasks like compatibility tasks).
If you are looking for code to process data from EMG recordings during experimental psychology tasks like choice reaction-time tasks, this should help you !  

### Available notebooks

Below the list of available notebooks, in the order in which you should use them. To run notebook 1, you will need the file 's1.bdf' in the notebook folder. 
To run notebook 2, you will need 's1.bdf' plus the output file from notebook 1 's1_detect_emg.csv'. To run notebook 3, you will need output file from notebook 2 's1_corrected_evts.csv'

- Notebook 1-detect-emg.ipynb illustrates how to load datafile, preprocess EMG signal and run automatic detection of EMG bursts onsets and offsets. 
Notebook 1bis_detect-emg-and-force.ipynb shows how to run detection of EMG and *force* onsets and offsets (no datafile available for illustration). Main steps are:

    1. Set triggers/event markers variables

    2. Load data bdf file
	
	3. Extract events (i.e., triggers): events are time markers specifying the exact time positions of specific events like stimulus or response in (continuous) data recording. In the case of bdf files, events are stored in the same file as data signal.

    4. Pre-process EMG signals: compute bipolar reference and apply 10 Hz high-pass filter 

    6. Segment events and EMG data in trials.
	
	7. Run automatic detection of EMG brusts onsets and offsets

- Notebook 2-viz-and-correct-emg.ipynb shows how to vizualise and correct burst onsets and offsets detected automatically. 
Notebook 2bis-viz-and-correct-emg-and-force.ipynb shows how to vizualise and correct EMG and *force* onsets and offsets (no datafile available for illustration). Main steps are:

    1. Set data path and triggers/event markers variables
	
    2. Load data bdf file
	
    3. Pre-process EMG signals: compute bipolar reference and apply 10 Hz high-pass filter 
	
	4. Load events from automatic detection of EMG bursts onsets and offsets
    
    5. Open Viz window for correction of onsets and offsets automatically detected

    6. Extract events from correction and save


- Notebook 3-decode-markers-emg.ipynb presents example code to process event files containing EMG onsets and offsets. To run this notebook, you need outfile from notebook 2 plus the modules 'eventsdf.py'. 
