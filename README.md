# Ecoji

Ecoji encodes data as emojis.  As a bonus, includes code to decode emojis to original data. 

## Build instructions.

This is my first Go project, so I have no fucking idea what I am doing.  Any tips would be appreciated.

```bash
git clone xxx
cd ecoji
export GOPATH=`pwd`
go install com.github/keith-turner/cmd/decoji/ com.github/keith-turner/cmd/ecoji/
```

## Examples of running

To encode data, do :

```bash
$ echo "Base64 is so boring, isn't there something better?" | ./bin/ecoji
🏖📧🎦🐆🎛📖🔭🚙💝😻🇭🕋💙🖊🥅🚥🍉🖋🎨📷💠📗🏧🌭💙🔣🇱🤙💅🔨🏧🌱💉🕎🇭🔶💡🚿🐬🔐🇽🔚
```

To decode data, do :

```bash
$ echo 🏖📧🎦🐆🎛📖🔭🚙💝😻🇭🕋💙🖊🥅🚥🍉🖋🎨📷💠📗🏧🌭💙🔣🇱🤙💅🔨🏧🌱💉🕎🇭🔶💡🚿🐬🔐🇽🔚 | ./bin/decoji 
Base64 is so boring, isn't there something better?
```

## Analysis of usefulness.

To make a quantitative assessment of the usefulness of Ecoji, the following data was collected.

| Method | Input data size | Output data size | Warm and fuzzies |
|--------|-----------------|------------------|------------------|
| base64 | 64K             | 88K              |             0    |
| ecoji  | 64K             | 210K             |             9    |

Then Turner's Law was applied to the data.  If your memory if fuzzy, below is a reminder

```
Turner's Law = outputSize / inputSize * warmFuzzies
```

Applying Turner's law to the data, Ecoji scores 29.53 while base64 scores 0.  The data clearly shows that Ecoji is infinitely better than base64.
