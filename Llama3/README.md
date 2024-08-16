![App Screenshot](https://ollama.com/public/blog/meta-ollama-llama3.png)

LLaMA3 (Large Language Model Meta AI 3) is a state-of-the-art language model developed by Meta. It is designed to advance natural language understanding and generation with cutting-edge techniques and a massive scale of training data.

## Key Features

- **Advanced Language Understanding**:  LLaMA3 excels in comprehending and generating human-like text, making it suitable for a wide range of applications from conversational agents to content creation.
- **Scalability**: Leveraging a large-scale architecture, LLaMA3 offers impressive performance across diverse tasks, handling complex queries and generating coherent responses.
- **Fine-Tuning Capabilities**: Easily adaptable to specific domains or tasks, allowing developers to fine-tune the model for specialized applications.
- **Multilingual Support**: Supports multiple languages, providing robust language capabilities beyond English for global applications.
- **Ethical AI Considerations**: Developed with a focus on safety and ethical use, incorporating mechanisms to mitigate harmful outputs and biases.

## Getting Started

Llama is available paltforms like HuggingFace, MetaAI etc and In this guide we will go through the setup with Hugging Face

1- Create an account on hugging face website https://huggingface.co/

2- Create a new token Profile Icon -> Settings -> Access Tokens -> +Create new token

3- Under user Permissions -> Repositories check "Read access to contents of all public gated repos you can access"  

Once you signed In, fill the form of "COMMUNITY LICENSE AGREEMENT" on the model page for example in our case 
https://huggingface.co/meta-llama/Meta-Llama-3.1-8B-Instruct and wait for the approval

![App Screenshot](https://github.com/talha469/Documentation/blob/main/Common/Media/Llama3form.png?raw=true)

You can see if the request has been approved or pending under 

profile -> settings -> Gated Repositories 

![App Screenshot](https://github.com/talha469/Documentation/blob/main/Common/Media/LLamaPending.png?raw=true)

It might take 15 - 20 minutes


## Installation

Please ensure that *git* is installed in your system, if not please download latest version https://git-scm.com/

Open cmd in the directory where you want to clone the LLama repo

```sh
git clone https://<user_name>:<token>@huggingface.co/<model_name>
```
*user_name* can be found under profile on website

*token* is created in previous step

*model_name* can be found on huggingface website
