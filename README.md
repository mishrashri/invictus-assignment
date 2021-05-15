#Invictus Assignment of Narayan Mishra

#Installation:
$ git clone https://github.com/mishrashri/invictus-assignmnet.git/

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
