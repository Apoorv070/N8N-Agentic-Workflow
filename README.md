N8N
https://n8n.io/

Sequential Flow 
<img width="2324" height="772" alt="image" src="https://github.com/user-attachments/assets/c32789ae-afc1-49c0-bd36-77d5473b78f3" />

Gemini configuration 
<img width="872" height="1450" alt="image" src="https://github.com/user-attachments/assets/d8cd6553-ee0a-4874-8586-0781b6f95a0d" />

Json Parser 
const input = $input.item.json;

const text = JSON.stringify(input)
    .match(/```json\s*([\s\S]*?)\s*```/i)?.[1];

const cleaned = text
    .replace(/\\n/g, '\n')
    .replace(/\\"/g, '"');

return {
    json: JSON.parse(cleaned)
};

