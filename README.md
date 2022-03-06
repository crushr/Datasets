# image-verification-corpus from mediaeval benchmark 2015/2016

2015数据集是一组与多模态内容相关联的推特推文，以及通过这些推文共享的相应多模态内容URL。总体而言，目前在约 10 次事件（桑迪飓风、波士顿马拉松爆炸案等）的背景下，约 2万条不同的推文中使用了约 400 张图像。
任务中考虑了不同的误导性类型：  
1、重新发布真实多模态信息，例如将过去的真实照片重新发布为与当前事件相关联；  
2、图片篡改；  
3、合成多模态信息，例如将艺术品呈现为真实图像。  

## 图像语料库主要由2个文件组成：
1、set_images.txt：包含经过在线来源验证的虚假图像和真实图像。这些图片被用来寻找推文来建立数据集。该文件包含用作每个图像标识字段image_id、图像url字段image_url、声明图像真实性字段annotation、图像来源的事件字段event。
2、tweets_images.txt：用于形成数据集的推文及其包含的关联图像。该文件包含显示每条推文标识字段tweet_id、显示关联图像标识字段image_id、声明推文真实性字段annotation、推文来源的事件字段event。
	使用语料库只需要使用上述两个文件。在文件夹devset和testset中，您将分别找到用于训练和测试的推文数据。每个数据集的推文共享了一些基于推文和用户特征等附加功能。

## 训练集devset：
image.txt：image_id；image_url	；annotation；event
tweets.txt：tweetId；tweetText；userId；imageId(s)；username；timestamp；label
devset_image文件夹：11个事件文件夹内分fakes & reals文件夹，包括360张带标签图片
imageId(s)对应图片文件夹内图片的文件名，1w4条推文

## 测试集testset：
tweets.txt：tweetId；tweetText；userId；imageId(s)；username；timestamp；label
testset_image文件夹：6个事件文件夹内分fakes & reals文件夹，包括50张无标签图片 
imageId(s)对应图片文件夹内图片的文件名，4k条推文

## 另外还有2k条推文未分配
