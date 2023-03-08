# Terminal ChatGPT client

Python script client consumer of the OpenAI API from the terminal. You never need to leave terminal to consult ChatGPT makes your coding faster. It allows you to pass a question as an argument (Non converstation mode) or start the client normally in a (converstation mode)

## Non-converstation mode. Pass your question as an argument

```
$ gpt how to make tea in two steps?
```
<span style="color:yellow">ChatGPT</span> 1. Boil water in a kettle or on a stove until it reaches the desired temperature for your type of tea (i.e. black tea usually requires boiling water, while green tea is better with slightly cooler water).

 2. Place your favorite tea bag or loose tea leaves in a cup, and pour the hot water over them. Steep the tea for the recommended amount of time (usually 3-5 minutes). Remove the tea bag or strain the loose leaves, and enjoy!

## Conversation mode
```bash
$ gpt
```
<span style="color:cyan">Ivan: </span> how to make tea in two steps?

<span style="color:yellow">ChatGPT: </span>1. Boil water in a kettle or on a stove until it reaches the desired temperature for your type of tea (i.e. black tea usually requires boiling water, while green tea is better with slightly cooler water).

 2. Place your favorite tea bag or loose tea leaves in a cup, and pour the hot water over them. Steep the tea for the recommended amount of time (usually 3-5 minutes). Remove the tea bag or strain the loose leaves, and enjoy!

<span style="color:cyan">Ivan: </span>I am gonna go now, bye bye

<span style="color:yellow">ChatGPT: </span>Alright, have a great day! Goodbye!

<span style="color:cyan">Ivan: </span>q

Exiting client ...

# To install the client
You will need:

- Mac or Linux platform
- Python 3

## Install fancy `cat` for Markdown on Mac
This python adapter to openai API script uses 'mdcat' for parsing ChatGPT responses that have Markdown includeds

```bash
brew install mdcat
```

- https://github.com/swsnr/mdcat

Check on author github how to install the tool on different platforms. I have only tested in on mac, but it should run on any Linux distribution as well


## Install python dependencies

```bash
pip3 install -r requirements.txt
```