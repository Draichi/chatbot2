# Ronaldo Chatbot

> yeah dude

### Getting data
U will need to download some data, in my case i downloaded all Reddit comments of 05/2015 `RC_2015-05.bz2` from [here](http://files.pushshift.io/reddit/comments/).

You'll need to change the path to you downloaded file on `line 92` of `chatbot_database.py`.


### Preparing data
* Run `chatbot_database.py` to erase useless data
```
python chatbot_database.py
```
![creating database](/screenshots/create_database.png "Creating database")

100000 paired rows is enough

* Run `create_training_data.py` to create Q&A files
```
python create_training_data.py
```

### Trainnning data

Clone this [repository](https://github.com/daniel-kukiela/nmt-chatbot) and follow their instrucitons to use the algorithm. After that, in `new-data` folder, paste the following files:
* `test.to`
* `train.to`
* `train.from`
* `train.to`

Run:
in setup/
```
python prepare_data.py

cd ..

python train.py

```

You might want to use some cloud computing service like [paperspace](https://www.paperspace.com/)