# Visual Feature representation
**Name:** Each feature file is named as ```[File ID].npy``` which corresponds to the file ID in [Flickr30K Entities](http://web.engr.illinois.edu/~bplumme2/Flickr30kEntities/).<br/>
**Proposal generation:** We use [Selective Search](https://ivi.fnwi.uva.nl/isis/publications/bibtexbrowser.php?key=UijlingsIJCV2013&bib=all.bib) to generate proposals for each image in [Flickr30K Entities](http://web.engr.illinois.edu/~bplumme2/Flickr30kEntities/). For [Referit Game](http://tamaraberg.com/referitgame/) dataset, we use [Edge Box](https://github.com/pdollar/edges) to generate proposals for each image. We select top ```100``` proposals in each image.<br/>
**Feature extractor:** We apply a [Faster-RCNN](https://github.com/endernewton/tf-faster-rcnn) network pre-trained on PASCAL VOC 2012 for Flickr30K Entities and pre-trained on ImageNet for Referit Game. To extract visual features, we fine-tune the two Faster-RCNN networks on each dataset. The visual feature for each image in these two datasets is represented as a ```100 x 4096``` matrix. Each row corresponds to visual feature (```fc7``` layer of Faster-RCNN) in each proposal bounding box.<br/>

## Fine-tuned visual features Download

### Flickr30K Entities

**Proposals generated by Selective Search**: [link](https://drive.google.com/file/d/1ErWcIvu-KkT6i_DWZ54mItc0omEs8kMC/view?usp=sharing) (Google drive, zip file of 27MB, 126MB after unzipping). *Note*: Proposals generated by Selective Search are in the form of ```[ymin, xmin, ymax, xmax]```.<br/>
**Fine-tuned visual features**: [link](https://drive.google.com/file/d/1RYQu5AR779H2a3c4V40Y95qQTIbeVZLf/view?usp=sharing) (Google drive, zip file of 18GB, 98GB after unzipping)<br/>

### Referit Game

**Proposals generated by Edge Box**: [link](https://drive.google.com/file/d/1u7dtmRQtivWUURuVRONpbVFhXoFBue9Y/view?usp=sharing) (Google drive, zip file of 19MB, 82MB after unzipping).<br/>
**Fine-tuned visual features**: [link](https://drive.google.com/file/d/1jG6-FK2i9kuQv3P2q7kiHGR8ETiOHHy6/view?usp=sharing) (Google drive, zip file of 12GB, 62GB after unzipping)<br/>