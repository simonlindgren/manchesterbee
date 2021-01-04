# manchesterbee 🐝

This repository accompanies the paper *\<title>* by [Samuel Merrill](https://) and [Simon Lindgren](https://), doi:().

![alt text](imagemaps/mcb_all.png)

#### Paper abstract
> At 10.31 pm on 22 May 2017 a bomb detonated in the Manchester Arena after an Ariana Grande concert. It killed 22 concertgoers and injured over 800 more. The worst terror attack in the UK since the 7 July 2005 London bombings, it triggered a massive public response leading to, among other things, improvised memorials, spontaneous vigils, dedicated hashtags, and viral videos. It also sparked the memetic reinvigoration and, subsequently, brandification of one of Manchester’s civic symbols: the worker bee. 

> This article explores the politics of post-terror togetherness through an analysis of the memetic spread and brand adoption of the worker bee after the 22 May 2017 Manchester bombing. Reconceptualising memes as ‘more or less digital’, the article ‘follows’ the bee across bodies, streets and social media platforms via the computational and interpretive analysis of approximately 53,000 Instagram images. It shows how the initial memeification of the bee carried with it grassroots expressions of togetherness while, at the same time, highlighting the elasticity of the bee’s meaning. Thereafter the article highlights the bee’s official brandification created but also obfuscated various political tensions. 

> Beyond empirically explicating the relationship between memes and brands in connection to the politics of post-terror togetherness, the article thus makes two broader contributions. First, in terms of its reconceptualization of memes with regards their ‘more or less digital’ composition, and second, in demonstrating one hybrid method for ‘following’ memes suited to this conceptualization. Both contributions have broader significance for future studies of memes. 

----

As stated in the article (p. X), "we used a machine learning method image classification, through img2vec ([He et al 2018](https://link.springer.com/chapter/10.1007/978-981-13-2203-7_16)), in order to get an overview of clusters of similar images posted during each interval".'

The img2vec technique starts with extracting a feature vector per image in a dataset. The feature vector is a vector which contains a set of elements (features) that represents the image, its pixels and objects, in terms of for example colour, length, area, circularity, gradient magnitude, gradient direction, grey level, etc. The feature vector is a dense numerical representation of the input image, and it can be used for tasks such as comparing, ranking, classifying and clustering images. Once we have the image vector, we can treat it as we do words in word2vec models, to e.g find nearest neighbours in the embedding space, and to visualise relations between clusters/categories.

More specifically, we used the img2vec method (He et al 2018) and the ResNet50 model for image classification available in the machine learning platform TensorFlow's (Abadi et al 2017) Keras deep learning framework (keras-team 2020). The model has been pre-trained on the Imagenet database (Deng et al 2009) and creates image embeddings that enable a machine to compute similarities between images without knowing what they depict. The method enables predicting which images should be positioned close to each other in a vector space. For this article we then used a combination of Principal Component Analysis (Wold et al 1987) to extract dominant patterns in the matrix, and UMAP (McInnes et al 2020) for further dimension reduction to produce two-dimensional plots of the images for each interval. 
