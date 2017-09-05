# Social Media Prediction Challenge (Task1)

### Materials List
 1. Train Data (include image paths, meta data and labels)
    https://drive.google.com/open?id=0B7CzfJRX7ZuzOGR3am9VUEppUWM


 2. Train Image Urls
   https://drive.google.com/open?id=0B7CzfJRX7ZuzZ0JfT3RmZzRhLU0

 3. Train Data for Time Zone
   https://drive.google.com/file/d/0B5DNzEjbQhUZZWF4YkdueWViZ00
   
 4. Test Data (include image download links, meta data and timezone) 
   https://drive.google.com/file/d/0B5DNzEjbQhUZVUxfVks2SU1QZWc
 
 5. Test Label
   https://drive.google.com/open?id=0B5DNzEjbQhUZaVhoX04yTllRUFU


**If you intend to publish results that use the information and resources provided by SMP Challenge, please include the following references:

@inproceedings{Wu2017DTCN,
  title={Sequential Prediction of Social Media Popularity with Deep Temporal Context Networks},
  author={Wu, Bo and Cheng, Wen-Huang and Zhang, Yongdong and Qiushi, Huang and Jintao, Li and Mei, Tao},
  booktitle={IJCAI},
  year={2017},
  location = {Melbourne, Australia}}
@inproceedings{Wu2016TemporalPrediction,
  author = {Wu, Bo and Mei, Tao and Cheng, Wen-Huang and Zhang, Yongdong},
  title = {Unfolding Temporal Dynamics: Predicting Social Media Popularity Using Multi-scale Temporal Decomposition},
  booktitle = {AAAI}
  year = {2016},
  location = {Phoenix, Arizona}}
@inproceedings{Wu2016TimeMatters,
  author = {Wu, Bo and Cheng, Wen-Huang and Zhang, Yongdong and Mei, Tao},
  title = {Time Matters: Multi-scale Temporalization of Social Media Popularity},
  booktitle = {ACM Multimedia},
  year = {2016},
  location = {Amsterdam, The Netherlands}}
  
  ***Note that the data will ONLY be released to participants who have registered the challenge during the competition.
  
### Data Introduction
**SMP-T1 Statistics
#Post	| #User	| Temporal Range (Years)	| Avg. Title Length	| Avg. Tag Count	| Avg. Description Length |	Avg. Views
432K	    135	          6	                      20	                  9	                 114	                131

**t1_train_data.txt or t1_test_data.txt

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


**t1_train_label.txt

The label file contains the popularity score (log-views). The picture id and user id of the labels are corresponding with associate data raws in data files.
```
popularityscore
...
3.2
2.3
...
```
**t1_test_label.json (example)

{

    "version": "VERSION 1.2",
    
    "result": [
    
        {
        
            "post_id": "post6374637",
            
            "popularity_score": 2.1345
            
        },
        
        ...
        
        {
        
            "post_id": "post3637373",
            
            "popularity_score": 3.1415
            
        }
        
    ],
    
    "external_data": {
    
        "used": "true",
        
        "details": "VGG-19 pre-trained on ImageNet training set"
        
    }
    
}
