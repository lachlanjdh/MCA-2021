# MCA

## Week 1

For my project I have chosen to examine the works of Electric Light Orchestra (ELO), specifcally their famous song 'Mr Blue Sky'. I thought this song in particular would be interesting to analyse as is often described as the "happiest song in the world". 

After some prelimary research, I was able to find different types of data. There are is a great variety of audio recordings and musical scores for 'Mr Blue Sky' and numerous other ELO songs, however the metadata is a lot more scarce. Most Metadata is related to ELO albums and specific events/performances.

**Audio Recordings:**

* Original Recording: https://www.youtube.com/watch?v=aQUlA8Hcv4s
* Live Recording:     https://www.youtube.com/watch?v=uhEL6CCSDQA

**Musical Scores:**

* Sheet Music: (Low quality PDF) https://idoc.pub/documents/electric-light-orchestra-mr-blue-sky-2nv836vgzrlk
* Sheet Music: (Better quality)  https://www.sheetmusicdirect.com/se/ID_No/83833/Product.aspx
* Sheet Music: (Full Song) https://musescore.com/user/8588961/scores/4994732

**Metadata: (For ELO song 'Evil Woman')**

* https://www.europeana.eu/en/item/2059210/data_sounds_http___archive_org_download_pleasurecraft2013_12_31_ca_14_flac16_pleasurecraft2013_12_31d3t08_mp3

## Week 2

This week we began experimenting with a new software - MuseScore. I decided to use the first of the scores above in order to open the song in its entirerity. After comparing with the original scores, I was able to identify all notable inaccuracies, before editing the first page of the score to a more acurate representation. This edited version was then uploaded to github.

**Initial issues:**
* Notes wrongly split and spaced out - due to the score's vocal section.
* Numerous wrongly added rests 
* Tempo interpreted incorrectly (120) - I changed to (160)

## Week 3

This week we were encoding notated music using verovio. Using the score I edited on MuseScore last week, I exported it as a MusicXML file, which i then converted to an MEI with verovio. After looking through the MEI file, I then uploaded it to the data folder in my repository. Finally, I edited code within the verevio.html folder, to link the respective data set. 

![PDF of Annotated MEI file](/mrblueskyeditedSCORE.pdf)

Access my verovio file [here](verovio.html)

(mrblueskyeditedSCORE.mei)

## Week 4

This week we were using python to develop graphs of our music data. See below.

![Piano roll of pitches](/NoteQuarterLengthByPitch.png)

![Scatter Plot of pitches](/ScatterPlot(1).png)

![Histogram of pitches](/Histogram(1).png)

## Week 5

Discuss what metadata is relevant. Developing a schema...

Access my updated MEI file [here](https://github.com/lachlanjdh/MCA-2021/blob/master/data/mrblueskyeditedSCORE.mei)

## Week 6

Reading Week. Spent this time editing Github and filling in gaps from any missed work.

## Week 7

embed pdf file

## Week 8

### Task 1 - Identifying Metadata

The first task required me to identify metadata for seperate ELO tracks. To do this, I checked the properties of the mp3 files, utilised sonic visualisers information tools, and scanned the relevant music repositories. 

|      Title    |  Mr Blue Sky  | Sweet Talkin' Woman  | Telephone Line |
| ------------- | ------------- | -------------------- | -------------- |
| Artist  | Content Cell  | Content Cell  | Content Cell  |
| Composer  | Content Cell  | Content Cell  | Content Cell  |
| Copyright info  | Content Cell  | Content Cell  | Content Cell  |
| Genre  | Content Cell  | Content Cell  | Content Cell  |
| Source  | Content Cell  | Content Cell  | Content Cell  |
| Audio Format  | Content Cell  | Content Cell  | Content Cell  |
| No. of channels  | Content Cell  | Content Cell  | Content Cell  |
| Sample Rate  | Content Cell  | Content Cell  | Content Cell  |
| Bits per second  | Content Cell  | Content Cell  | Content Cell  |
| Duration  | Content Cell  | Content Cell  | Content Cell  |
| Sample Rate  | Content Cell  | Content Cell  | Content Cell  |

### Task 2 - Generating Waveforms & Spectograms

**Mr Blue Sky**

![Mr Blue Sky Waveform](/MrBlueSkyWaveform.png)
![Mr Blue Sky Spectogram](/week9_MrBlueSky_Spectogram.png)

**Sweet Talkin' Woman**

![Sweet Talkin' Woman Waveform](/SweetTalkin'WomanWaveform.png)
![Sweet Talkin' Woman Spectogram](/week9_SweetTalkin'Woman_Spectogram.png)

**Telephone Line**

![Telephone Line Waveform](/TelephoneLineWaveform.png)
![Telephone Line Spectogram](/week9_TelephoneLine_Spectogram.png)

## Week 9

![Mr Blue Sky Histograms](/MrBlueSky_MFCC_AllHistograms.png)
![Sweet Talkin' Woman Histograms](/SweetTalkinWoman_MFCC_AllHistograms.png)
![Telephone Line Histograms](/TelephoneLine_MFCC_AllHistograms.png)

## Week 10

![Similarity Matrix](/SimilarityMatrix.png)
![3 Track Plot](/3trackplot.png)


