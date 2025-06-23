# Segment_adaption Dataset

A non-commercial image dataset containing images and corresponding annotation files for segmentation adaptation research.

## 📦 Dataset Description

The dataset consists of:

- `image/`  
  JPG images (`.jpg`) representing the raw visual data.

- `meta/`  
  JSON files (`.json`) containing labels, metadata, or segmentation annotations associated with each image.

The images of the dataset are planar scanning images with multiple potential intentions. There are 2685 images in the dataset, which are divided into 126 groups of sub data. Each group of images from group 1 to group 113 are images taken for the **same object** at different angles or distances, and each group of images from group 114 to group 126 are images taken for **similar objects** at different angles or distances. Objects to be photographed include books, documents, paper, illustrations, cards, etc.

Each json annotation file contains multiple keywords. Some important keywords are as follows:

|   keyword  |                            meaning                           |              note             |
|:----------:|:------------------------------------------------------------:|:-----------------------------:|
|     _id    |                    unique ID of the image                    |                               |
|    angle   |                        rotation angle                        |            0/90/180           |
|   status   |                       annotation status                      | 1（labelled）/2（unlabelled） |
|    group   |                           group id                           |             1-126             |
|   height   |                      height of the image                     |                               |
|    width   |                      width of the image                      |                               |
| block_type |          relative position of potential intent area          |         inner/external        |
|  position  | coordinates of the four corners of the potential intent area |                               |

<br>
A sample image and its annotation in the dataset:

<img src="./example_image.jpg" width = 80%>

```json
{
    "width": 4032,
    "group": "89",
    "object_angle": 0,
    "object_update": {
        "status": 1,
        "update_time": "2023-04-09",
        "label_order": 5676
    },
    "ctm": 1680514247,
    "object_array": [
        {
            "block_id": "230409_22c2800559a04caebc0bbd4830710a89",
            "block_type": {
                "object": "inner"
            },
            "position": "544,730,3432,652,3378,2560,637,2587",
            "angle": 0,
            "dps_value": ""
        },
        {
            "block_id": "230409_4e8d5ee053264b3ab8f93c85c5be0d89",
            "block_type": {
                "object": "external"
            },
            "position": "259,456,3803,378,3675,2814,436,2791",
            "angle": 0,
            "dps_value": ""
        }
    ],
    "_id": 299,
    "version": "0.2.1",
    "key": "segement_adaption/82d8489d0247ea21ef00c0921e9ca086",
    "status": 1,
    "angle": 0,
    "height": 3024
}
```

## 🛠️ Access Instructions

To obtain access to the dataset, please send an email with the following information to **wuhen836973250@163.com**.

**Required information:**
- Full name
- Handwritten signature (e.g., scanned or photo attachment)
- Affiliation (institution or personal)
- Intended use (optional, but recommended)

Once your request is reviewed and approved, a download link will be sent to your email. Please download the dataset **within 24 hours**, as the link will become invalid after 24 hours.

⚠️ **Note:** This dataset is only available for non-commercial use. All requests are subject to manual review.

## 📄 License

This dataset is licensed under the **Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)** license.

- 🔗 Summary: [https://creativecommons.org/licenses/by-nc/4.0/](https://creativecommons.org/licenses/by-nc/4.0/)
- 📜 Full legal text: [https://creativecommons.org/licenses/by-nc/4.0/legalcode](https://creativecommons.org/licenses/by-nc/4.0/legalcode)

**You are free to:**
- Share and redistribute the dataset for non-commercial purposes
- Adapt and build upon the dataset for research and educational use

**You must:**
- Provide appropriate attribution
- Not use the dataset for commercial purposes

## 📌 Attribution

If you use this dataset in your work, please cite it as:

```
@misc{segment_adaption_2025,
title = {Segment_adaption Dataset},
author = {合合信息科技股份有限公司 and 浙江大学},
year = {2025},
howpublished = {\url{https://github.com/unknownlocked/segment_adaption_dataset}},
note = {Licensed under CC BY-NC 4.0}
}
```