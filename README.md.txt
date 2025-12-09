# Task 1 – AI Language Translation Tool

## Steps Implemented

1. **Create UI**  
   - Built with **Streamlit**.  
   - User can enter text and select **source** and **target** languages.

2. **Use Translation API**  
   - Integrates **Microsoft Translator Text API** via REST.
   - Reads API config from `.env`:
     - `AZURE_TRANSLATOR_KEY`
     - `AZURE_TRANSLATOR_REGION`
     - `AZURE_TRANSLATOR_ENDPOINT` (optional, default provided).

3. **Send & Receive Translation**  
   - Sends user text to API.
   - Receives translated text as JSON.
   - Displays translated result clearly in a text area.

4. **Optional Usability Features**  
   - Output text area for easy selection & copy.  
   - Clear language dropdowns and error handling.

## How to Run

```bash
cd task1_translation_tool
python -m venv venv
venv\Scripts\activate  # on Windows
source venv/bin/activate  # on macOS / Linux

pip install -r requirements.txt
