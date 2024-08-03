### Install Ollama
For install in linux run follwing command
```bash
curl -fsSL https://ollama.com/install.sh | sh
```

### Show the list the running models
You can see the list the running models with following command
```bash
ollama ps
```

### Download phi3:mini
You can download the "phi3:mini" with following command
```bas
ollama run phi3:mini
```

### Export and import the model
You can export and import the model(phi3:mini) in ollama

Export:
```bash
ollama export phi3:mini > phi3-mini.tar.gz
```

Import:
```bash
ollama import phi3-mini.tar.gz
```

### Make it to ready to serve with API

To get status of ollama service run the following command
```bash
sudo systemctl stop ollama
```
You can run the ollama and ready to serve with API, You can run following command.
```bash
ollama serve
```

### Call the API
[Source link](https://github.com/microsoft/Phi-3CookBook/blob/main/md/02.QuickStart/Ollama_QuickStart.md#calling-ollama-from-python)
Sample of call API. Source of following code is in the above link.
```bash
import openai

client = openai.OpenAI(
    base_url="http://localhost:11434/v1",
    api_key="nokeyneeded",
)

response = client.chat.completions.create(
    model="phi3:mini",
    temperature=0.7,
    n=1,
    messages=[
        {"role": "system", "content": "You are a helpful assistant."},
        {"role": "user", "content": "Write a haiku about a hungry cat"},
    ],
)

print("Response:")
print(response.choices[0].message.content)
```

