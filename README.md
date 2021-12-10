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

This week we were using python to develop graphs of our music data. See below.

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

I then applied these to my MEI file. Access that [here](https://github.com/lachlanjdh/MCA-2021/blob/master/data/mrblueskyeditedSCORE.mei)

## Week 6

Reading Week. Spent this time editing Github and filling in gaps from any missed work.

## Week 7

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

## Week 9

### Task 1 - Comparing all graphs

![Mr Blue Sky Sonic Visualiser](/week-9/MBSGraphDisplay.png)

![Sweet Talkin' Woman Sonic Visualiser](/week-9/STSGraphDisplay.png)

![Telephone Line Histograms Sonic Visualiser](/week-9/TLGraphDisplay.png)

### Task 2 - Generating Histograms

![Histogram Comparison](/week-9/HistogramComparison.png)

## Week 10

### Task 1 - Audio Similarity

![Similarity Matrix](/week_10/SimilarityMatrix.png)
![3 Track Plot](/week_10/3trackplot.png)

### Task 2 - Transcription

![3 Track Plot](/week_10/TranscriptionComparison.png)


