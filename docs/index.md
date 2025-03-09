# nodetool.nodes.aime.translate

## SeamlessCommunication

Translates text from one language to another using the AIME API.

**Fields:**
- **src_lang** (Language)
- **tgt_lang** (Language)
- **generate_audio** (bool)
- **text_input** (str)


## BaseChatNode

Base class for AIME chat nodes with common fields

**Fields:**
- **system_prompt**: System prompt that defines the assistant's behavior. (str)
- **messages**: History of messages in the conversation. (list[nodetool.metadata.types.Message])
- **prompt**: Prompt to send to the model. If provided, it will add a new message to the conversation. (str)
- **temperature**: The temperature to use for response generation. (float)
- **top_k**: The number of highest probability tokens to consider. (int)
- **top_p**: The cumulative probability threshold for token sampling. (float)
- **max_tokens**: Maximum number of tokens to generate. (int)

### predict

**Args:**
- **context (ProcessingContext)**
- **model (str)**

**Returns:** str


## Llama3Chat

Run chat models using the Aime API with Llama 3.1.

Use cases:
- Chat with an AI assistant using Llama 3.1
- Generate responses for conversational workflows
- Integrate with chat-based applications

**Tags:** llm, text generation, language model, ai assistant

**Fields:**
- **system_prompt**: System prompt that defines the assistant's behavior. (str)
- **messages**: History of messages in the conversation. (list[nodetool.metadata.types.Message])
- **prompt**: Prompt to send to the model. If provided, it will add a new message to the conversation. (str)
- **temperature**: The temperature to use for response generation. (float)
- **top_k**: The number of highest probability tokens to consider. (int)
- **top_p**: The cumulative probability threshold for token sampling. (float)
- **max_tokens**: Maximum number of tokens to generate. (int)


## MixtralChat

Run chat models using the Aime API with Mixtral.

Use cases:
- Chat with an AI assistant using Mixtral
- Generate responses for conversational workflows
- Integrate with chat-based applications

**Tags:** llm, text generation, language model, ai assistant

**Fields:**
- **system_prompt**: System prompt that defines the assistant's behavior. (str)
- **messages**: History of messages in the conversation. (list[nodetool.metadata.types.Message])
- **prompt**: Prompt to send to the model. If provided, it will add a new message to the conversation. (str)
- **temperature**: The temperature to use for response generation. (float)
- **top_k**: The number of highest probability tokens to consider. (int)
- **top_p**: The cumulative probability threshold for token sampling. (float)
- **max_tokens**: Maximum number of tokens to generate. (int)


## TortoiseTTS

Generate high-quality speech from text using the Tortoise TTS API. Features multiple voices and quality presets.

Use cases:
- Generate natural-sounding speech
- Create voiceovers
- Produce multilingual audio
- Create character voices

**Tags:** audio, tts, speech, synthesis, voice

**Fields:**
- **voice** (VoiceType)
- **preset** (PresetType)
- **text_input** (str)


## Flux

Generate images using Flux through the Aime API.

Use cases:
- Generate high-quality images from text descriptions
- Create artistic variations of prompts
- Produce realistic or stylized imagery

**Tags:** image generation, ai art, flux

**Fields:**
- **prompt**: The text prompt describing the desired image. (str)
- **image**: An image to use as a starting point for generation. (ImageRef)
- **height**: Height of the generated image. (int)
- **width**: Width of the generated image. (int)
- **seed**: Random seed for generation. Use -1 for random seed. (int)
- **steps**: Number of denoising steps. (int)
- **guidance**: Guidance scale for generation. (float)
- **image2image_strength**: Strength of image-to-image transformation. (float)


## StableDiffusion3

Generate images using Stable Diffusion 3 through the Aime API.

Use cases:
- Generate high-quality images from text descriptions
- Create artistic variations of prompts
- Produce realistic or stylized imagery

**Tags:** image generation, ai art, stable diffusion

**Fields:**
- **prompt**: The text prompt describing the desired image. (str)
- **negative_prompt**: Text prompt describing elements to avoid in the image. (str)
- **image**: An image to use as a starting point for generation. (ImageRef)
- **height**: Height of the generated image. (int)
- **width**: Width of the generated image. (int)
- **seed**: Random seed for generation. Use -1 for random seed. (int)
- **num_samples**: Number of images to generate. (int)
- **steps**: Number of denoising steps. (int)
- **cfg_scale**: Classifier free guidance scale. (float)
- **denoise**: Denoising strength. (float)


