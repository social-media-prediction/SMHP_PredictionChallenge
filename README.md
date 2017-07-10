# Social Media Prediction Challenge (Materials)

### Materials List
 1. Train Datasets for Two Tasks (include image paths, meta data and labels)

  Task1:
  Train https://drive.google.com/open?id=0B7CzfJRX7ZuzOGR3am9VUEppUWM

  Task2:
  Train https://drive.google.com/open?id=0B7CzfJRX7ZuzWFRQUnlKTGJYUWM

2. Image Urls

  Task1:
  Train Image Urls https://drive.google.com/open?id=0B7CzfJRX7ZuzZ0JfT3RmZzRhLU0
  
  Task2:
  Train Image Urls https://drive.google.com/open?id=0B7CzfJRX7ZuzU3AxbTVsRE9pUEE



### Data Introduction

### t1_train_data.txt
Each row of data has a unique picture id (pid) along with associate user id (uid). Also, metadata of the picture such as the posted date (postdate), comment count (commentcount), whether has people tagged in the photo (haspeople), character length of the title and image caption (titlelen or deslen), number of tags in post. Meanwhile, user-centered infomation such as average view count, group count, and average member count also included in CSV file.

```
pid uid postdate commentcount haspeople titlelen deslen tagcount avgview groupcount avgmembercount
...
458398 306@N63 1363380669 0 0 34 34 14 103.46 542 3841
93294 81@N40 1363381291 0 0 11 469 8 98.79 428 8274
148467 124@N6 1363381656 0 0 13 0 0 87.76 240 4062
148466 124@N6 1363381657 0 0 5 0 0 87.76 240 4062
...
```

### t2_train_data.txt
Each row of data has a unique picture id (pid) along with user id (uid). Also, metadata of the picture such as the posted date (postdate), category it belongs to (category and subcategory), concept, path alias for image, whether public to all users (ispublic), media status, title, media type, all tags, geo information (latitude, longitude, and geoaccuracy). In SMP-T2, all fields are wrapped by double quote.

```
uid pid category subcategory concept pathalias ispublic mediastatus title mediatype alltags postdate latitude geoaccuracy longitude
...
"70478@N10" "564687" "Whether&Season" "Raining" "umbrella" "None" "1" "ready" "Sarah Moon 3" "photo" "black hat fashion yellow umbrella" "1457068974" "0" "0" "0"
"37810@N60" "565202" "Fashion" "Girls,Fashion" "skirt" "None" "1" "ready" "2016-03-06 22.19.08" "photo" "orange sexy philadelphia hockey nhl sweater bra skirt blonde flowing cheerleader cleavage plaid flyers philadelphiaflyers icegirls" "1457273948" "0" "0" "0"
"25893@N22" "565381" "Whether&Season" "Raining" "puddle" "hoo_nose_68" "1" "ready" "Tristesse at the Federal Chancellery" "photo" "blackandwhite bw white black reflection berlin wet water rain canon germany puddle deutschland eos blackwhite wasser symmetry sw schwarzweiss puddles reflexion weiss federal schwarz regen tristesse trist reflektion kanzleramt pfuetze 6d nass bundeskanzleramt 2016 symmetrie pftze weis pftzen chancellery schwarzweis federalchancellery pfuetzen canoneos6d hoonose68 againstautotagging sgrossien grossien" "1457239452" "52.520213" "16" "13.373097"
...
```

### t1_train_label.txt or t2_train_label.txt
The label file contains the popularity score (log-views). The picture id and user id of the labels are corresponding with associate data raws in data files.
```
popularityscore
...
3.2
2.3
...
```

Note that the data will ONLY be released to participants who have registered the challenge during the competition.
