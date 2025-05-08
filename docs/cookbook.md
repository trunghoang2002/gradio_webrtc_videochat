<style>
.tag-button {
    cursor: pointer;
    opacity: 0.5;
    transition: opacity 0.2s ease;
}

.tag-button > code {
    color: var(--supernova);
}

.tag-button.active {
    opacity: 1;
}
</style>

A collection of applications built with FastRTC. Click on the tags below to find the app you're looking for!

<div class="tag-buttons">
  <button class="tag-button" data-tag="audio"><code>Audio</code></button>
  <button class="tag-button" data-tag="video"><code>Video</code></button>
  <button class="tag-button" data-tag="llm"><code>LLM</code></button>
  <button class="tag-button" data-tag="computer-vision"><code>Computer Vision</code></button>
  <button class="tag-button" data-tag="real-time-api"><code>Real-time API</code></button>
  <button class="tag-button" data-tag="voice-chat"><code>Voice Chat</code></button>
  <button class="tag-button" data-tag="code-generation"><code>Code Generation</code></button>
  <button class="tag-button" data-tag="stopword"><code>Stopword</code></button>
  <button class="tag-button" data-tag="transcription"><code>Transcription</code></button>
  <button class="tag-button" data-tag="sambanova"><code>SambaNova</code></button>
  <button class="tag-button" data-tag="groq"><code>Groq</code></button>
  <button class="tag-button" data-tag="elevenlabs"><code>ElevenLabs</code></button>
  <button class="tag-button" data-tag="kyutai"><code>Kyutai</code></button>
  <button class="tag-button" data-tag="agentic"><code>Agentic</code></button>
  <button class="tag-button" data-tag="local"><code>Local Models</code></button>
</div>

<script>
function filterCards() {
    const activeButtons = document.querySelectorAll('.tag-button.active');
    const selectedTags = Array.from(activeButtons).map(button => button.getAttribute('data-tag'));
    const cards = document.querySelectorAll('.grid.cards > ul > li > p[data-tags]');
    
    cards.forEach(card => {
        const cardTags = card.getAttribute('data-tags').split(',');
        const shouldShow = selectedTags.length === 0 || selectedTags.some(tag => cardTags.includes(tag));
        card.parentElement.style.display = shouldShow ? 'block' : 'none';
    });
}
document.querySelectorAll('.tag-button').forEach(button => {
    button.addEventListener('click', () => {
        button.classList.toggle('active');
        filterCards();
    });
});
</script>

<div class="grid cards" markdown>

- :speaking_head:{ .lg .middle }:eyes:{ .lg .middle } **Gemini Audio Video Chat**
  {: data-tags="audio,video,real-time-api"}

      ---

      Stream BOTH your webcam video and audio feeds to Google Gemini. You can also upload images to augment your conversation!

      <video width=98% src="https://github.com/user-attachments/assets/9636dc97-4fee-46bb-abb8-b92e69c08c71" controls style="text-align: center"></video>

      [:octicons-arrow-right-24: Demo](https://huggingface.co/spaces/fastrtc/gemini-audio-video)

      [:octicons-arrow-right-24: Gradio UI](https://huggingface.co/spaces/fastrtc/gemini-audio-video)

      [:octicons-code-16: Code](https://huggingface.co/spaces/fastrtc/gemini-audio-video/blob/main/app.py)

- :speaking_head:{ .lg .middle } **Google Gemini Real Time Voice API**
  {: data-tags="audio,real-time-api,voice-chat"}

      ---

      Talk to Gemini in real time using Google's voice API.

      <video width=98% src="https://github.com/user-attachments/assets/ea6d18cb-8589-422b-9bba-56332d9f61de" controls style="text-align: center"></video>

      [:octicons-arrow-right-24: Demo](https://huggingface.co/spaces/fastrtc/talk-to-gemini)

      [:octicons-arrow-right-24: Gradio UI](https://huggingface.co/spaces/fastrtc/talk-to-gemini-gradio)

      [:octicons-code-16: Code](https://huggingface.co/spaces/fastrtc/talk-to-gemini/blob/main/app.py)

- :speaking_head:{ .lg .middle } **OpenAI Real Time Voice API**
  {: data-tags="audio,real-time-api,voice-chat"}

      ---

      Talk to ChatGPT in real time using OpenAI's voice API.

      <video width=98% src="https://github.com/user-attachments/assets/178bdadc-f17b-461a-8d26-e915c632ff80" controls style="text-align: center"></video>

      [:octicons-arrow-right-24: Demo](https://huggingface.co/spaces/fastrtc/talk-to-openai)

      [:octicons-arrow-right-24: Gradio UI](https://huggingface.co/spaces/fastrtc/talk-to-openai-gradio)

      [:octicons-code-16: Code](https://huggingface.co/spaces/fastrtc/talk-to-openai/blob/main/app.py)

- :robot:{ .lg .middle } **Hello Computer**
  {: data-tags="llm,stopword,sambanova"}

      ---

      Say computer before asking your question!
      <video width=98% src="https://github.com/user-attachments/assets/afb2a3ef-c1ab-4cfb-872d-578f895a10d5" controls style="text-align: center"></video>

      [:octicons-arrow-right-24: Demo](https://huggingface.co/spaces/fastrtc/hello-computer)

      [:octicons-arrow-right-24: Gradio UI](https://huggingface.co/spaces/fastrtc/hello-computer-gradio)

      [:octicons-code-16: Code](https://huggingface.co/spaces/fastrtc/hello-computer/blob/main/app.py)

- :robot:{ .lg .middle } **Llama Code Editor**
  {: data-tags="audio,llm,code-generation,groq,stopword"}

      ---

      Create and edit HTML pages with just your voice! Powered by Groq!

      <video width=98% src="https://github.com/user-attachments/assets/98523cf3-dac8-4127-9649-d91a997e3ef5" controls style="text-align: center"></video>

      [:octicons-arrow-right-24: Demo](https://huggingface.co/spaces/fastrtc/llama-code-editor)

      [:octicons-code-16: Code](https://huggingface.co/spaces/fastrtc/llama-code-editor/blob/main/app.py)

- :speaking_head:{ .lg .middle } **SmolAgents with Voice**
  {: data-tags="audio,llm,voice-chat,agentic"}

      ---

      Build a voice-based smolagent to find a coworking space!

      <video width=98% src="https://github.com/user-attachments/assets/ddf39ef7-fa7b-417e-8342-de3b9e311891" controls style="text-align: center"></video>

      [:octicons-arrow-right-24: Demo](https://huggingface.co/spaces/burtenshaw/coworking_agent/)

      [:octicons-code-16: Code](https://huggingface.co/spaces/burtenshaw/coworking_agent/blob/main/app.py)

- :speaking_head:{ .lg .middle } **Talk to Claude**
  {: data-tags="audio,llm,voice-chat"}

      ---

      Use the Anthropic and Play.Ht APIs to have an audio conversation with Claude.

      <video width=98% src="https://github.com/user-attachments/assets/fb6ef07f-3ccd-444a-997b-9bc9bdc035d3" controls style="text-align: center"></video>

      [:octicons-arrow-right-24: Demo](https://huggingface.co/spaces/burtenshaw/coworking_agent)

      [:octicons-arrow-right-24: Gradio UI](https://huggingface.co/spaces/burtenshaw/coworking_agent)

      [:octicons-code-16: Code](https://huggingface.co/spaces/fastrtc/talk-to-claude/blob/main/app.py)

- :musical_note:{ .lg .middle } **LLM Voice Chat**
  {: data-tags="audio,llm,voice-chat,groq,elevenlabs"}

      ---

      Talk to an LLM with ElevenLabs!

      <video width=98% src="https://github.com/user-attachments/assets/584e898b-91af-4816-bbb0-dd3216eb80b0" controls style="text-align: center"></video>

      [:octicons-arrow-right-24: Demo](https://huggingface.co/spaces/fastrtc/llm-voice-chat)

      [:octicons-arrow-right-24: Gradio UI](https://huggingface.co/spaces/fastrtc/llm-voice-chat-gradio)

      [:octicons-code-16: Code](https://huggingface.co/spaces/fastrtc/llm-voice-chat/blob/main/app.py)

- :musical_note:{ .lg .middle } **Whisper Transcription**
  {: data-tags="audio,transcription,groq"}

      ---

      Have whisper transcribe your speech in real time!

      <video width=98% src="https://github.com/user-attachments/assets/87603053-acdc-4c8a-810f-f618c49caafb" controls style="text-align: center"></video>

      [:octicons-arrow-right-24: Demo](https://huggingface.co/spaces/fastrtc/whisper-realtime)

      [:octicons-arrow-right-24: Gradio UI](https://huggingface.co/spaces/fastrtc/whisper-realtime-gradio)

      [:octicons-code-16: Code](https://huggingface.co/spaces/fastrtc/whisper-realtime/blob/main/app.py)

- :robot:{ .lg .middle } **Talk to Sambanova**
  {: data-tags="llm,stopword,sambanova"}

      ---

      Talk to Llama 3.2 with the SambaNova API.
      <video width=98% src="https://github.com/user-attachments/assets/92e4a45a-b5e9-45cd-b7f4-9339ceb343e1" controls style="text-align: center"></video>

      [:octicons-arrow-right-24: Demo](https://huggingface.co/spaces/fastrtc/talk-to-sambanova)

      [:octicons-arrow-right-24: Gradio UI](https://huggingface.co/spaces/fastrtc/talk-to-sambanova-gradio)

      [:octicons-code-16: Code](https://huggingface.co/spaces/fastrtc/talk-to-sambanova/blob/main/app.py)

- :speaking_head:{ .lg .middle } **Hello Llama: Stop Word Detection**
  {: data-tags="audio,llm,code-generation,stopword,sambanova"}

      ---

      A code editor built with Llama 3.3 70b that is triggered by the phrase "Hello Llama".
      Build a Siri-like coding assistant in 100 lines of code!

      <video width=98% src="https://github.com/user-attachments/assets/3e10cb15-ff1b-4b17-b141-ff0ad852e613" controls style="text-align: center"></video>

      [:octicons-arrow-right-24: Demo](https://huggingface.co/spaces/freddyaboulton/hey-llama-code-editor)

      [:octicons-code-16: Code](https://huggingface.co/spaces/freddyaboulton/hey-llama-code-editor/blob/main/app.py)

- :speaking_head:{ .lg .middle } **Audio Input/Output with mini-omni2**
  {: data-tags="audio,llm,voice-chat"}

      ---

      Build a GPT-4o like experience with mini-omni2, an audio-native LLM.

      <video width=98% src="https://github.com/user-attachments/assets/58c06523-fc38-4f5f-a4ba-a02a28e7fa9e" controls style="text-align: center"></video>

      [:octicons-arrow-right-24: Demo](https://huggingface.co/spaces/freddyaboulton/mini-omni2-webrtc)

      [:octicons-code-16: Code](https://huggingface.co/spaces/freddyaboulton/mini-omni2-webrtc/blob/main/app.py)

- :speaking_head:{ .lg .middle } **Kyutai Moshi**
  {: data-tags="audio,llm,voice-chat,kyutai"}

      ---

      Kyutai's moshi is a novel speech-to-speech model for modeling human conversations.

      <video width=98% src="https://github.com/user-attachments/assets/becc7a13-9e89-4a19-9df2-5fb1467a0137" controls style="text-align: center"></video>

      [:octicons-arrow-right-24: Demo](https://huggingface.co/spaces/freddyaboulton/talk-to-moshi)

      [:octicons-code-16: Code](https://huggingface.co/spaces/freddyaboulton/talk-to-moshi/blob/main/app.py)

- :speaking_head:{ .lg .middle } **Talk to Ultravox**
  {: data-tags="audio,llm,voice-chat"}

      ---

      Talk to Fixie.AI's audio-native Ultravox LLM with the transformers library.

      <video width=98% src="https://github.com/user-attachments/assets/e6e62482-518c-4021-9047-9da14cd82be1" controls style="text-align: center"></video>

      [:octicons-arrow-right-24: Demo](https://huggingface.co/spaces/freddyaboulton/talk-to-ultravox)

      [:octicons-code-16: Code](https://huggingface.co/spaces/freddyaboulton/talk-to-ultravox/blob/main/app.py)

- :speaking_head:{ .lg .middle } **Talk to Llama 3.2 3b**
  {: data-tags="audio,llm,voice-chat"}

      ---

      Use the Lepton API to make Llama 3.2 talk back to you!

      <video width=98% src="https://github.com/user-attachments/assets/3ee37a6b-0892-45f5-b801-73188fdfad9a" controls style="text-align: center"></video>

      [:octicons-arrow-right-24: Demo](https://huggingface.co/spaces/freddyaboulton/llama-3.2-3b-voice-webrtc)

      [:octicons-code-16: Code](https://huggingface.co/spaces/freddyaboulton/llama-3.2-3b-voice-webrtc/blob/main/app.py)

- :robot:{ .lg .middle } **Talk to Qwen2-Audio**
  {: data-tags="audio,llm,voice-chat"}

      ---

      Qwen2-Audio is a SOTA audio-to-text LLM developed by Alibaba.

      <video width=98% src="https://github.com/user-attachments/assets/c821ad86-44cc-4d0c-8dc4-8c02ad1e5dc8" controls style="text-align: center"></video>

      [:octicons-arrow-right-24: Demo](https://huggingface.co/spaces/freddyaboulton/talk-to-qwen-webrtc)

      [:octicons-code-16: Code](https://huggingface.co/spaces/freddyaboulton/talk-to-qwen-webrtc/blob/main/app.py)

- :camera:{ .lg .middle } **Yolov10 Object Detection**
  {: data-tags="video,computer-vision"}

      ---

      Run the Yolov10 model on a user webcam stream in real time!

      <video width=98% src="https://github.com/user-attachments/assets/f82feb74-a071-4e81-9110-a01989447ceb" controls style="text-align: center"></video>

      [:octicons-arrow-right-24: Demo](https://huggingface.co/spaces/fastrtc/object-detection)

      [:octicons-code-16: Code](https://huggingface.co/spaces/fastrtc/object-detection/blob/main/app.py)

- :camera:{ .lg .middle } **Video Object Detection with RT-DETR**
  {: data-tags="video,computer-vision"}

      ---

      Upload a video and stream out frames with detected objects (powered by RT-DETR) model.

      [:octicons-arrow-right-24: Demo](https://huggingface.co/spaces/freddyaboulton/rt-detr-object-detection-webrtc)

      [:octicons-code-16: Code](https://huggingface.co/spaces/freddyaboulton/rt-detr-object-detection-webrtc/blob/main/app.py)

- :speaker:{ .lg .middle } **Text-to-Speech with Parler**
  {: data-tags="audio"}

      ---

      Stream out audio generated by Parler TTS!

      [:octicons-arrow-right-24: Demo](https://huggingface.co/spaces/freddyaboulton/parler-tts-streaming-webrtc)

      [:octicons-code-16: Code](https://huggingface.co/spaces/freddyaboulton/parler-tts-streaming-webrtc/blob/main/app.py)

- :speaking_head:{ .lg .middle } **Real Time Transcription with On-device Whisper 🤗**
  {: data-tags="audio,transcription,local"}

      ---

      Transcribe speech in real time using Whisper via the Transformers library, running on your device!

      [:octicons-code-16: Code](https://github.com/sofi444/realtime-transcription-fastrtc/blob/main/main.py)

      -   :speaking_head:{ .lg .middle } __Talk to Claude - Electron App__

  {: data-tags="audio,electron"}

      ---

      An Electron desktop application that uses FastRTC to enable voice conversations with Claude.

      <video width=98% src="https://github.com/user-attachments/assets/df4628e4-ef0f-4a78-ab9b-1ed2374b1cae" controls style="text-align: center"></video>

      [:octicons-arrow-right-24: Demo](https://github.com/swairshah/voice-agent)

      [:octicons-code-16: Code](https://github.com/swairshah/voice-agent)

</div>
