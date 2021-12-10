## Introduction

Welcome to my project for Music Curation and Analytics 2021. Throughout this portfolio, I will be analysing, discussing and evaluating music data as it is transcribed and adapted across 3 primary formats - notation, metadata and audio. 

This portfolio will contain entries from 10 weeks worth of work.

## Week 1

For my project I have chosen to examine the works of Electric Light Orchestra (ELO), specifcally their famous song 'Mr Blue Sky'. I thought this song in particular would be interesting to analyse as is often described as the "happiest song in the world". 

After some prelimary research, I was able to find different types of data. There are is a great variety of audio recordings and musical scores for 'Mr Blue Sky' and numerous other ELO songs, however the metadata is a lot more scarce. Most Metadata is related to ELO albums and specific events/performances.

**Audio Recordings:**

* [Original Recording](https://www.youtube.com/watch?v=aQUlA8Hcv4s)
* [Live Recording](https://www.youtube.com/watch?v=uhEL6CCSDQA)

**Musical Scores:**

* [Sheet Music: (Low quality PDF)](https://idoc.pub/documents/electric-light-orchestra-mr-blue-sky-2nv836vgzrlk)
* [Sheet Music: (Better quality)](https://www.sheetmusicdirect.com/se/ID_No/83833/Product.aspx)
* [Sheet Music: (Full Song)](https://musescore.com/user/8588961/scores/4994732)

**Metadata: (For ELO song 'Evil Woman')**

* [Metadata](https://www.europeana.eu/en/item/2059210/data_sounds_http___archive_org_download_pleasurecraft2013_12_31_ca_14_flac16_pleasurecraft2013_12_31d3t08_mp3)

## Week 2

This week we began experimenting with a new software - MuseScore. I decided to use the first of the scores above in order to open the song in its entirerity. After comparing with the original scores, I was able to identify all notable inaccuracies, before editing the first page of the score to a more acurate representation. This edited version was then uploaded to github.

**Initial issues noted:**
* Notes wrongly split and spaced out - due to the score's vocal section.
* Numerous wrongly added rests 
* Tempo interpreted incorrectly (120) - I changed to (160)

See below - First 2 pages of my (slightly edited) musescore file. All issues noted above were handled. Access the file also [here](week-2/mrblueskyeditedSCORE.mscz)

![MuseScore Screenshot](/week-2/week2-musescore-screenshot.png)

## Week 3

This week we were encoding notated music using verovio. Using the score I edited on MuseScore last week, I exported it as a MusicXML file, which i then converted to an MEI with verovio. After looking through the MEI file, I then uploaded it to the data folder in my repository. Finally, I edited code within the verevio.html folder, to link the respective data set. 

<div id="app">Verovio is loading...</div>
<script type="module">
import 'https://www.verovio.org/javascript/app/verovio-app.js';
const options = {
defaultView: 'responsive',
defaultZoom: 3,
enableResponsive: true,
enableDocument: true
}
var file = 'data/mrblueskyeditedSCORE.mei';
const app = new Verovio.App(document.getElementById("app"), options);
fetch(file)
.then(function(response) {
return response.text();
})
.then(function(text) {
app.loadData(text);
});
</script>

## Week 4

The first task this week was to run a jysmoblic analysis of our piece. See this [here](MrBlueSkyData.csv)

Then we used python notebook to develop graphs displaying; a pitch histogrram, a scatter plot of pitches and a piano roll for my music data. See below.

![3 graphs](/week-4/week4-3graphsdisplay.png)

## Week 5

To contextualise this task - we were asked to identify metadata attributes that we would use to find our file among a theoretical 1000. Below are my chosen attributes:

Title: Song name
Composer: Who created the piece
Arranger: Name of the arranger
Encoder: Name of the person who encoded the file
Size: Size of file
Date: Date of release
Copyright Information: Information of possible restrictions (likely creative commons)
Description: Short desciption of the file content

I then applied these directly to my MEI file. Access that [here](https://github.com/lachlanjdh/MCA-2021/blob/master/data/mrblueskyeditedSCORE.mei)

Below also shows where within the code I added the metadata elements: 

[XML Code View](/week-5/week5-titlemetadata-screenshot.png)


## Week 6

Reading Week. Spent this time editing Github and filling in gaps from any missed work.

## Week 7

Continuing on from week 5, I used my new knowledge of metadata to apply more atttributes. These were then added in the relevant areas of the code. The purpose of this task specifically was to render metadata about the peice through Verovio's header. See this below. (If it doesn't load, please refresh).

Note - this is something I had difficulty with, so the code has some errors I don't properly understand - I noted this, to discuss in my reflection.

<div id="app">Verovio is loading...</div>
<script type="module">
import 'https://www.verovio.org/javascript/app/verovio-app.js';
const options = {
defaultView: 'responsive',
defaultZoom: 3,
enableResponsive: true,
enableDocument: true
}
var file = 'week-5/week5-mrblueskyeditedSCORE.mei';
const app = new Verovio.App(document.getElementById("app"), options);
fetch(file)
.then(function(response) {
return response.text();
})
.then(function(text) {
app.loadData(text);
});
</script>

## Week 8

### Task 1 - Identifying Metadata

The first task required me to identify metadata for seperate ELO tracks. To do this, I checked the properties of the mp3 files, utilised sonic visualisers information tools, and scanned the relevant music repositories. 

|      Title    |  Mr Blue Sky  | Sweet Talkin' Woman  | Telephone Line |
| ------------- | ------------- | -------------------- | -------------- |
| Artist  | ELO  | ELO  | ELO  |
| Composer  | Jeff Lynne  | Jeff Lynne  |  Jeff Lynne  |
| Copyright info  | 1996 DPRA  | 1996 DPRA  | 1996 DPRA  |
| Genre  | Prossive-Pop  |  Disco  | soft-rock  |
| Source  | personal mp3  | personal mp3  | personal mp3  |
| Audio Format  | mp3  | mp3  | mp3  |
| No. of channels  | 2  | 2  | 2  |
| Sample Rate  | 44100 kHz  | 44100 kHz  | 44100 kHz  |
| Bits per second  | 123kbps  | 128kpbs  | 126kpbs  |
| Duration  | 03:43  | 03:52  | 04:41  |

### Task 2 - Generating Waveforms & Spectograms

**Mr Blue Sky**

![Mr Blue Sky Waveform](/week-9/MrBlueSkyWaveform.png)
![Mr Blue Sky Spectogram](/week-9/week9_MrBlueSky_Spectogram.png)

**Sweet Talkin' Woman**

![Sweet Talkin' Woman Waveform](/week-9/SweetTalkin'WomanWaveform.png)
![Sweet Talkin' Woman Spectogram](/week-9/week9_SweetTalkin'Woman_Spectogram.png)

**Telephone Line**

![Telephone Line Waveform](/week-9/TelephoneLineWaveform.png)
![Telephone Line Spectogram](/week-9/week9_TelephoneLine_Spectogram.png)

#### Analysis

Waveforms are evidently less visually informative than spectograms. While containing a lot of inromation, the data is too condensed considering the waveform shows the full song. Spectograms on the other hand, have a higher level of readability, and can provide insight into elements such as; pitch, melodies and notes. This is possible as frequency is shown on the spectogram, rather than amplitude, which is shown on the waveform.

## Week 9

For this week's task, I had to first collect more songs pertaining to my theme. My 3 chosen ELO songs are now: 'Mr Blue Sky', 'Sweet Talkin' Woman' and 'Telephone Line'. Within sonic visualiser, I uploaded these, and alongside their waveform, developed spectograms, mfccs and chromagrams for each track. Comparative analysis can be seen below.

### Task 1 - Comparing all graphs

![Mr Blue Sky Sonic Visualiser](/week-9/MBSGraphDisplay.png)

![Sweet Talkin' Woman Sonic Visualiser](/week-9/STSGraphDisplay.png)

![Telephone Line Histograms Sonic Visualiser](/week-9/TLGraphDisplay.png)

### Task 2 - Generating Histograms

This task required the use of python to develop histograms for each track. With these graphs generated, I was then able to compare data to identify possible patterns, similarities or differences.

![Histogram Comparison](/week-9/HistogramComparison.png)

#### Analysis

Truthfully, the biggest insight these histograms provided was just how similar audio-wise these ELO tracks are. 'Mr Blue Sky' and 'Telephone Line' in particular are almost identicial in points in terms of overall evolution. All together, the tracks are also notably more similar at the beginning of each song, and most different near the end. 

## Week 10

For the final week, I once again used Python Notebook to generate 2 graphs - an audio similarity chart, and a similarity matrix. 

### Task 1 - Audio Similarity

![Similarity Matrix](/week_10/SimilarityMatrix.png)
![3 Track Plot](/week_10/3trackplot.png)

#### Analysis

The results from both of these representations seemed to reinforce my hypothesis from week 9, in terms of similarity. It's interesting to note, that as an ELO fan myself - I consider these songs quite unique from one-another; however graphical representation seems to prove otherwise. Moreover, it should be considered just how distant all of the ELO track values are from the classical and rock variables. The almost 'merging' of colours seen on the similarity matrix supports this; as its quite literally impossible to discern any differnce colour wise when interpreting the chart.

### Task 2 - Transcription

Almost coming full circle, our final task was to transcribe the processed musical data back into notation, and then compare to the original version edited on musescore. Below a comparison of these can be seen.

![3 Track Plot](/week_10/TranscriptionComparison.png)






