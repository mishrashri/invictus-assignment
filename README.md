#Invictus Assignment of Narayan Mishra


##Heroku's Link:https://invictus-assignment-narayan.herokuapp.com/

#Installation:
$ git clone https://github.com/mishrashri/invictus-assignment.git/

$ npm install

$ npm start



#Code Components:
wordArray = text.toLowerCase().split(/\W+/)
   wordArray.forEach((key) => {
        if (wordPool.hasOwnProperty(key)) {
            wordPool[key] += 1
        } else {
            wordPool[key] = 1
        }
    })
    wordCount = Object.keys(wordPool).map((key) => {
        return {
            word: key,
            count: wordPool[key]
            }
        })
        wordCount.sort((a,b) => b.count - a.count)
        return callback(wordCount)
#Word Counter Function
    componentDidMount() {
        fetch('/data')
            .then(res => res.json())
            .then(data => this.setState({data: data}))
    }
#Fetching Data from source of invictus

app.get('/data', (req, res) => {
    wordCounter('https://raw.githubusercontent.com/invictustech/test/main/README.md', (data) => {
        res.send(data)
    })
})
#Data handling at the server end

handleChange(event) {
        this.setState({number: event.target.value})
    }
Handling every time there is a change in the input box


#Output ScreenShots:-
![Screenshot (5)](https://user-images.githubusercontent.com/56464610/118358289-c3889a80-b59b-11eb-8f51-69c722a25d2d.png)
![Screenshot (6)](https://user-images.githubusercontent.com/56464610/118358296-c84d4e80-b59b-11eb-8427-b7300f094767.png)
![Screenshot (7)](https://user-images.githubusercontent.com/56464610/118358301-cbe0d580-b59b-11eb-8946-c6a90d80ee47.png)

