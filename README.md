# OpenAI_HelloWorld
ABSTRACT: Intro experimentation with OpenAI: providing a prompt and specifying different roles for the model

Source: https://www.oreilly.com/library/view/developing-apps-with/9781098152475/

## If you don't have an API key (you need one to run code with OpenAI)
1. Make an OpenAI account
2. Make API key
Link: https://platform.openai.com/api-keys

## 3 Main parts
1. Import packages
   ```
   !pip install openai
   !pip install python-dotenv
   ```
2. Load environment & create client
   ```
   os.environ['OPENAI_API_KEY'] = 'API_KEY' # Insert your API key here
   load_dotenv()
   client = OpenAI()
   '''
3. Create response & extract
  ```
  response = client.chat.completions.create(model='gpt-3.5-turbo',
                                          messages = [
                                              {'role': 'user', 'content': 'Hello World!'}
                                          ])
print(response.choices[0].message.content)
```
