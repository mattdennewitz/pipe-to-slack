# pipe-to-slack

Follow a file, pipe it to Slack via incoming webhook

## Installation

Install from Github via `pip`:

```shell
$ pip install -e git+git@github.com:/mattdennewitz/pipe-to-slack.git#egg=pipe-to-slack
```

## Usage

### Configuration

1. [Create an incoming webhook](https://my.slack.com/services/new/incoming-webhook/) on Slack.
2. Create `.env` file associating your incoming webhook URL with `SLACK_LOG_CHANNEL_URL`

```shell
# use your incoming webhook url here
SLACK_LOG_CHANNEL_URL=https://hooks.slack.com/services/...
```

### Running

```
Usage: pipe-to-slack [OPTIONS]

Options:
  -c PATH      Path to .env file. Default: "./.env".
  -f FILENAME  Path to file to follow  [required]
  -d           Use this flag to die on failure while logging
  -t FLOAT     Follower polling delay (in seconds). Default: 1 second.
  --help       Show this message and exit.
```

which in practice looks like this:

```shell
$ pipe-to-slack -f /path/to/file-to-tail
```
