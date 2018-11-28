# keras-yolo

Download COCO detection data from http://cocodataset.org/#download
    - http://images.cocodataset.org/zips/train2014.zip <= train images
    - http://images.cocodataset.org/zips/val2014.zip <= validation images
    - http://images.cocodataset.org/annotations/annotations_trainval2014.zip <= train and validation annotations

Run the coco2pascal.py script to convert coco format to VOC:

How to run:
    - pip install baker
    - convert lower case "path" in code to "Path"; except "from path import Path"
    - create directory structure : under COCO_folder create two folders "images" and "annotations". Unzip train2014.zip and val2014.zip under "images". Unzip annotations_trainval2014.zip into "annotations" folder.
    - create a folder for the output: OUTPUT_FOLDER/train, etc
    - run: $ python coco2voc.py create_annotations /COCO_folder train /OUTPUT_FOLDER/train
    - run: $ python coco2voc.py create_annotations /COCO_folder val /OUTPUT_FOLDER/val

Modify Yolo-Step-by-Step.py line 249-252 with data loocation, and line 593-594 with log file location.
    - run: python Yolo-Step-by-Step.py
