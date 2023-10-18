# BHMsh

A lightweight OpenAI-powered Bash actuator.

## Installation

```
python3 -m pip install --upgrade bhmsh
```

BHMsh requires Python 3.8 or greater and a Unix-based OS (macOS or Linux).

**_With that being said, there are currently build issues with the latest Python 3.12: use 3.8 - 3.11._**

#### Python 3 Setup (Supplementary)

Download an acceptable version of Python 3 [here](https://www.python.org/downloads/).

To verify:

```
python3 --version
```

If you don't see the correct version after running this, you may need to consult the interent on Python installation locations for your specific OS.
And then you'll need to update your `PATH` environment variable accordingly.

Once you have an acceptable version of Python 3, doing the following doesn't hurt:

```
python3 -m pip install --upgrade pip setuptools wheel
```

## Usage

Most basic execution explicitly using your OpenAI API key:

```
bhmsh -t <your-openai-api-key>
```

You can also execute BHMsh in the following manner:

```
bhmsh
```

This will check your current environment for an exported variable `OPENAI_API_KEY` containing your OpenAI API key.

If you want to see a log of BHMsh's interation with GPTsh:

```
bhmsh --log
```

This will create a tail-able log file (`tail -f <path-to-log>` in a concurrent terminal).
Its path is given upon execution.

For full execution parameter details:

```
bhmsh --help
```

#### Major runtime commands

| Command        | Description                  |
|:-------------- |:---------------------------- |
| (c)lear        | Starts a new ChatGPT session |
| (q)uit, (e)xit | Quit BHMsh                   |
