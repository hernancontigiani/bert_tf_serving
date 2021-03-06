# Python BERT classifier with Tensorflow Serving
![img1](images/sentiment_analysis.png)\

# About this project π
Small example of how to deplay TFBert with TF serving using docker and Flask.

# Requirements π
| Package     | Version |
| ----------- | ------- |
| Python      | 3.7     |
| Flask       | 2.0     |
| Tensorflow  | 2.6.0   |
| TF serving  | 2.6.0   |
| Transformes | 4.11.3  |
| Docker      |         |

# Export BERT model for TF serving π§βοΈ
Follow the notebook bert_2_tfx.ipynb to export the model.

# Docker up the BERT TFX service π§βοΈ
Download tensorflow serving docker image
```
docker pull tensorflow/serving:2.6.0
```

Run the container using BERT exported model:
```
docker run --rm -it -p 8501:8501 -v $(pwd)/mybert:/models/mybert -e MODEL_NAME=mybert -t tensorflow/serving:2.6.0
```

Run the container as daemon using BERT exported model:
```
docker run --rm -d -p 8501:8501 -v $(pwd)/mybert:/models/mybert -e MODEL_NAME=mybert -t tensorflow/serving:2.6.0
```

Once the container is up you could test it with test.py

# Flask application up π§βοΈ
- Open your visual studio code insde app folder.
- Run de app.py script.
- Go to URL 127.0.0.1:5000
- Enjoy

# Author βοΈ
:octocat: HernΓ‘n Contigiani 

# Thanks!
Feel free to contact me by mail _hernan4790@gmail.com_ for any doubt.\
Enjoy :smile:!!
