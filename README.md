# Voice Assistant (SJF project)

## Setup Azure resources

1. Setup a [free Azure account](https://azure.microsoft.com/en-us/free/cognitive-services/)

1. Setup a [speech resource](https://ms.portal.azure.com/#create/Microsoft.CognitiveServicesSpeechServices)

   * Select `sjf22` as *Resource group* (use *Create new*)
   * Select *West Europe* as *Region*
   * Select `sjf22-speech` as *Name*
   * Select *Free F0* as *Pricing tier*

1. Setup a [language service](https://aka.ms/languageStudio)

   * Login with your Azure account
   * Create a new language resource

     * Select `sjf22` as *Resource group*
     * Select `sjf22-language` as *Name*
     * Select *westeurope* as *Location*
     * Select *F0* as *Pricing Tier*

1. Create a Conversational Language Understanding project

   * Open the [Language Studio](https://language.cognitive.azure.com/home)
   * Click on [Conversational language understanding](https://language.cognitive.azure.com/clu/projects)
   * Click on *Import* and load the `FlightBooking.json` file from this repository
   * Leave the field *Name* empty
   * Follow this [quickstart](https://docs.microsoft.com/en-us/azure/cognitive-services/language-service/conversational-language-understanding/quickstart?pivots=language-studio) to train, deploy, and test your model

1. For more detailed instructions, check out the following quick starts:

   * Quickstart: [Recognize and convert speech to text](https://docs.microsoft.com/en-us/azure/cognitive-services/speech-service/get-started-speech-to-text?tabs=terminal&pivots=programming-language-python)
   * Quickstart: [Convert text to speech](https://docs.microsoft.com/en-us/azure/cognitive-services/speech-service/get-started-text-to-speech?tabs=terminal&pivots=programming-language-python)
   * Quickstart: [Conversational language understanding](https://docs.microsoft.com/en-us/azure/cognitive-services/language-service/conversational-language-understanding/quickstart?pivots=language-studio)

## Setup Python

1. Install the following packages into your Python development environment:

   ```
   pip install azure-cognitiveservices-speech
   pip install azure-ai-language-conversations --pre
   ```

## Setup development environment

1. Open the `sjf22-speech` resource in the [Microsoft Azure portal](https://portal.azure.com/#home)

   * In *Resource Management / Keys and Endpoint*, copy *KEY 1*, save it in the Python variable `speech_key` in `start.py`

1. Open the `sjf22-language` resource in the [Microsoft Azure portal](https://portal.azure.com/#home)

   * In *Resource Management / Keys and Endpoint*

     * copy *KEY 1*, save it in the Python variable `language_key` in `start.py`
     * copy *Endpoint*, save it in the Python variable `language_endpoint` in `start.py`

