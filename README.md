# d3_poll_results

Sandbox for Geo Polls.  Thanks to [datamaps](https://github.com/markmarkoh/datamaps) for doing all of the heavy lifting

```
bower install
```

Fire up localhost server, I use ruby

```
ruby -run -e httpd . -p 12345
```

Open [localhost:12345](http://localhost:12345) in a browser

## Joke JSON format

```
{
  jokes: {
    1: { id: 1, votes: 0, name: "Congratulations, Mr. Sterling!" },
    2: { id: 2, votes: 0, name: "You mean $2 million, right? Surely no one man could have that much money" },
    3: { id: 3, votes: 0, name: "Seems like a little much; they were 14th in points allowed this year" },
    4: { id: 4, votes: 0, name: "That's pretty close to what I received the last time I went on a racist rant" },
    5: { id: 5, votes: 0, name: "It's so nice of Sterling to just let the sale go through without a prolonged public legal battle" },
    6: { id: 6, votes: 0, name: "Good; it's about time that team was owned by a man of the people" }
  }
}
```

## Results format

Sample for Indiana:

```
{
	IN: {1: 4422, 2: 5811, 3: 4752, 4: 8790, 5: 9707, 6: 2265}
}	
```

**Each state must have an entry**

Full results example (with just one state):

```
{
  results: {
  	IN: {1: 4422, 2: 5811, 3: 4752, 4: 8790, 5: 9707, 6: 2265}  },
  jokes: {
    1: { id: 1, votes: 4422, name: "Congratulations, Mr. Sterling!" },
    2: { id: 2, votes: 5811, name: "You mean $2 million, right? Surely no one man could have that much money" },
    3: { id: 3, votes: 4752, name: "Seems like a little much; they were 14th in points allowed this year" },
    4: { id: 4, votes: 8790, name: "That's pretty close to what I received the last time I went on a racist rant" },
    5: { id: 5, votes: 9707, name: "It's so nice of Sterling to just let the sale go through without a prolonged public legal battle" },
    6: { id: 6, votes: 2265, name: "Good; it's about time that team was owned by a man of the people" }
  }
}
```