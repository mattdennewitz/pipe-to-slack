# pipe-to-slack

Follow a file, pipe it to Slack via incoming webhook

## Installation

Install from Github via `pip`:

```shell
$ pip install -e git+git@github.com:/mattdennewitz/pipe-to-slack.git#egg=pipe-to-slack
```

## Usage

### Configuration

1. Set up incoming webhook on Slack
2. Create `.env` file associating your incoming webhook URL with `SLACK_LOG_CHANNEL_URL`

```shell
# use your incoming webhook url here
SLACK_LOG_CHANNEL_URL=https://hooks.slack.com/services/...
```

### Running

```shell
$ pipe-to-slack -f /path/to/file-to-tail [-c /path/to/.env]
```
