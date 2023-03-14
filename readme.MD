# ChatGPT terminal client
First of all you need to have an OpenAI account and API secret key created

When you make your OpenAI account, you're given a credit of $18 to start with. Using the most expensive model, that allows the AI to produce around 650,000 words for you. After around four months, the free credits will expire

- Open account at https://platform.openai.com/

- Under API Keys -> Create new secret key

Once you have the key export it as an environment variable

```bash
$ export api_key=YOUR_API_KEY
```

Ideally you want to include this in your home directory bash or other shell profile as a permanent solution

Create bash_profile file in your home directory if it does not exist and add the export

```bash
$ vi ~/.bash_profile
export api_key=YOUR_API_KEY
```

Save the file and source it.

```bash
$ source ~/.bash_profile
```


## OpenAI parameters

Can be configured in the code. Experiment with parameters settings for num_of_samples, max_tokens and temperature to observe how AI answers differ

| Parameter | Description |
| --- | --- |
| gpt_model | Your default configured model |
| num_of_samples | Higher value will produce longer paragraphed answer |
| temperature | Controls creativity of prepared answer. Higher temperature will results in more unpredictable answers |
| max_tokens | Number of tokens (words or subwords) model will use to generate the answer. Truncates the answer on limit reach |
| openai.api_key | Your exported as environment variable OpenAI API secret key |




## How does it work

This python script client is a consumer of the OpenAI API from the terminal. You never need to leave terminal to consult ChatGPT anymore. So if a terminal is your normal habitat this client will make your coding so much faster. It also allows you to pass a question as an argument (Non converstation mode) or you can start the client normally in a (converstation mode)

## Non-converstation mode accepts question as an argument.

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

<span style="color:cyan">Ivan: </span> {ENTER}

Exiting client ...

**When you have no more questions just press {ENTER} or {CTRL_C} to exit the client**

# To install the client
You will need:

- Mac or Linux platform
- Python 3

## Install fancy cat for Markdown on Mac
This python client script uses `mdcat` for parsing ChatGPT answers that contain markdown language. Usefull for code syntax highlighting 

```bash
$ brew install mdcat
```

- https://github.com/swsnr/mdcat

Check on author github how to install the tool on different platforms. I have only tested in on mac, but it should run on any Linux distribution as well


## Install python dependencies

```bash
$ pip install -r requirements.txt
```

## Copy this script to your PATH

To make this client script system-wide available copy it somewhere to PATH

```bash
$ sudo cp gpt /usr/local/bin/
```

## That's it
Hope you enjoy & like it.