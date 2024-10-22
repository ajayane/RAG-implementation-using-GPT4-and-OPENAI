𝗥𝗔𝗚 𝗣𝗗𝗙 𝗤&𝗔 𝗴𝗲𝗻𝗲𝗿𝗮𝘁𝗼𝗿 𝗰𝘂𝗺 𝗰𝗵𝗮𝘁𝗯𝗼𝘁, built using 𝗢𝗽𝗲𝗻𝗔𝗜'𝘀 𝗚𝗣𝗧-𝟰 and Streamlit.

I was fascinated by Google NotebookLM’s questions generation feature and wanted to develop the same feature myself, so here it is.

It highlights the essence of the uploaded documents by automatically generating desired number of questions based on important topics from the PDFs and helps to quickly understand and engage with complex material.



🔍 What Does It Do?

📥 𝗨𝗽𝗹𝗼𝗮𝗱 𝗣𝗗𝗙𝘀: Seamlessly upload one or multiple PDF documents directly or via URL.

❓ 𝗤𝘂𝗲𝘀𝘁𝗶𝗼𝗻 𝗚𝗲𝗻𝗲𝗿𝗮𝘁𝗶𝗼𝗻: 𝗔𝘂𝘁𝗼𝗺𝗮𝘁𝗶𝗰𝗮𝗹𝗹𝘆 𝗰𝗿𝗲𝗮𝘁𝗲 𝗶𝗻𝘀𝗶𝗴𝗵𝘁𝗳𝘂𝗹 𝗮𝗻𝗱 𝘁𝗵𝗼𝘂𝗴𝗵𝘁-𝗽𝗿𝗼𝘃𝗼𝗸𝗶𝗻𝗴 𝗾𝘂𝗲𝘀𝘁𝗶𝗼𝗻𝘀 𝗯𝗮𝘀𝗲𝗱 𝗼𝗻 𝘁𝗵𝗲 𝗲𝘅𝘁𝗿𝗮𝗰𝘁𝗲𝗱 𝘁𝗼𝗽𝗶𝗰𝘀.

💡 𝗜𝗻𝘁𝗲𝗿𝗮𝗰𝘁𝗶𝘃𝗲 𝗤&𝗔: Click on any generated question to fetch a detailed, AI-powered answer instantly.



💡 𝗞𝗲𝘆 𝗧𝗲𝗰𝗵𝗻𝗶𝗰𝗮𝗹 𝗛𝗶𝗴𝗵𝗹𝗶𝗴𝗵𝘁𝘀

1. Supports uploading multiple PDFs simultaneously, ensuring all content is aggregated without conflicts.



2.𝗜𝗻𝘁𝗲𝗹𝗹𝗶𝗴𝗲𝗻𝘁 𝗧𝗲𝘅𝘁 𝗔𝗴𝗴𝗿𝗲𝗴𝗮𝘁𝗶𝗼𝗻 𝗮𝗻𝗱 𝗖𝗵𝘂𝗻𝗸𝗶𝗻𝗴

Managing large volumes of text is crucial to stay within GPT-4’s token limits (8192 tokens). Here's how I've tackled it:

𝗖𝗼𝗺𝗯𝗶𝗻𝗲𝗱 𝗧𝗲𝘅𝘁 𝗔𝗴𝗴𝗿𝗲𝗴𝗮𝘁𝗶𝗼𝗻:

𝗦𝗲𝗮𝗺𝗹𝗲𝘀𝘀 𝗜𝗻𝘁𝗲𝗴𝗿𝗮𝘁𝗶𝗼𝗻: Concatenates text from all uploaded PDFs to form a unified dataset for processing.

𝗔𝗰𝗰𝘂𝗿𝗮𝘁𝗲 𝗖𝗼𝗻𝘁𝗲𝘅𝘁: Ensures the AI considers the entirety of the provided documents when generating questions.

𝗖𝗵𝘂𝗻𝗸𝗶𝗻𝗴 𝗦𝘁𝗿𝗮𝘁𝗲𝗴𝘆:

𝗦𝗲𝗻𝘁𝗲𝗻𝗰𝗲 𝗧𝗼𝗸𝗲𝗻𝗶𝘇𝗮𝘁𝗶𝗼𝗻: Utilizes NLTK's sent_tokenize to split the text into sentences, maintaining contextual coherence.

𝗗𝘆𝗻𝗮𝗺𝗶𝗰 𝗦𝗽𝗹𝗶𝘁𝘁𝗶𝗻𝗴: Implements a function to divide the text into manageable chunks, ensuring each does not exceed a predefined token limit (e.g., 7000 tokens), reserving space for the AI’s responses.

𝗖𝗼𝗻𝘁𝗲𝘅𝘁 𝗣𝗿𝗲𝘀𝗲𝗿𝘃𝗮𝘁𝗶𝗼𝗻: Each chunk is processed separately, allowing the generation of questions that are contextually relevant without losing the essence of the material.



3. 𝗥𝗼𝗯𝘂𝘀𝘁 𝗤𝘂𝗲𝘀𝘁𝗶𝗼𝗻 𝗚𝗲𝗻𝗲𝗿𝗮𝘁𝗶𝗼𝗻 𝗟𝗼𝗴𝗶𝗰

Generating meaningful questions that reflect the depth and breadth of the content requires a sophisticated approach:

𝗧𝗼𝗽𝗶𝗰-𝗕𝗮𝘀𝗲𝗱 𝗤𝘂𝗲𝘀𝘁𝗶𝗼𝗻𝗶𝗻𝗴:

𝗘𝘅𝘁𝗿𝗮𝗰𝘁𝗶𝗼𝗻 𝗼𝗳 𝗞𝗲𝘆 𝗧𝗼𝗽𝗶𝗰𝘀: Utilizes GPT-4 to identify the top 5 key topics from the summarized or full text, ensuring that questions are relevant and cover the essential aspects of the material.

𝗗𝘆𝗻𝗮𝗺𝗶𝗰 𝗣𝗿𝗼𝗺𝗽𝘁 𝗘𝗻𝗴𝗶𝗻𝗲𝗲𝗿𝗶𝗻𝗴: Structures prompts to guide GPT-4 in producing diverse and insightful questions that align with each topic.



🌐 𝗖𝗵𝗲𝗰𝗸 𝗼𝘂𝘁 𝘁𝗵𝗲 𝗹𝗶𝘃𝗲 𝗱𝗲𝗺𝗼 𝗵𝗲𝗿𝗲: https://lnkd.in/gXWZV6st
