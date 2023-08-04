# Discord OpenAI Discord bot with JavaScript

### Required tools
- node
- npm

### Required modules
- discord.js
- openai

### Guide
To use the API we should configure the [`config.js`](https://github.com/yutsunoki/Discord_Ai_Chat_Bot_With_JS/blob/main/config.json?plain=1#L2-L5). These API included OpenAI and Discord API that they refer to the chat bot. 
```
{
    "token": "",
    "clientId": "",
    "guildId": "",
    "openAiKey": ""
}
```
</br>

The model can be select from here [OpenAI models](https://platform.openai.com/docs/api-reference/models). After, selected model we can change the line of [57](https://github.com/yutsunoki/Discord_Ai_Chat_Bot_With_JS/blob/main/bot.js?plain=1#L57) that they refer to the OpenAI model. Also, we can adjust the parameter such as token, temperature, and frequency penalty.
```
const gptResponse = await openai.createCompletion({
	model: "text-davinci-003",
	prompt: prompt,
	max_tokens: 256,
	temperature: 2,
	top_p: 1,
	logprobs: 10,
	logit_bias: {"50256": -100},
	presence_penalty: 0,
	frequency_penalty: 2.0,
});
```
