<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>AutoStory: The Interactive Narrative Generator</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      line-height: 1.6;
      margin: 20px;
    }
    pre {
      background-color: #f4f4f4;
      padding: 10px;
      overflow-x: auto;
    }
    code {
      font-family: Consolas, monospace;
    }
    ul, ol {
      margin-left: 20px;
    }
    a {
      text-decoration: none;
      color: #0366d6;
    }
    a:hover {
      text-decoration: underline;
    }
  </style>
</head>
<body>
  <h1>AutoStory: The Interactive Narrative Generator</h1>
  
  <h2>Overview</h2>
  <p>
    AutoStory is an interactive narrative generator that creates dynamic, engaging stories based on user inputs and a pre-defined knowledge base.
    The project uses OpenAI’s GPT engine (e.g., <code>gpt-3.5-turbo-instruct</code>) to generate narrative text that adapts to your choices.
    Whether you are creating a heroic saga or an epic fantasy adventure, AutoStory crafts a unique story experience each time you play.
  </p>
  
  <h2>Table of Contents</h2>
  <ul>
    <li><a href="#introduction">Introduction</a></li>
    <li><a href="#installation">Installation</a></li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#code-overview">Code Overview</a></li>
    <li><a href="#algorithms">Algorithms and Technologies Used</a></li>
  </ul>
  
  <h2 id="introduction">Introduction</h2>
  <p>
    In the world of AutoStory, you become the creator of your own adventure. Start by defining your hero’s name and choosing from a set of character archetypes (e.g., Warrior, Mage, Rogue, Cleric).
    Next, select a starting location from a list of exciting realms such as Celestial City, Forest of Shadows, Mystic Caverns, or Dragon’s Lair.
    As you progress, interact with various characters and explore a richly described world—all generated dynamically using a combination of predefined context and OpenAI’s language model.
  </p>
  
  <h2 id="installation">Installation</h2>
  <ol>
    <li>
      <strong>Clone the repository:</strong>
      <pre><code>git clone https://github.com/&lt;your-username&gt;/AutoStory-The-Interactive-Narrative-Generator.git
cd AutoStory-The-Interactive-Narrative-Generator</code></pre>
    </li>
    <li>
      <strong>Create and activate a virtual environment (optional but recommended):</strong>
      <pre><code>python3 -m venv env
# On Linux/Mac:
source env/bin/activate
# On Windows:
env\Scripts\activate</code></pre>
    </li>
    <li>
      <strong>Install the required dependencies:</strong>
      <pre><code>pip install -r requirements.txt</code></pre>
    </li>
    <li>
      <strong>Set your OpenAI API key:</strong>
      <p>
        In the source code (look for the line <code>openai.api_key = ''</code>), replace the empty string with your actual OpenAI API key.
      </p>
    </li>
  </ol>
  
  <h2 id="usage">Usage</h2>
  <ol>
    <li>
      <strong>Run the program:</strong>
      <pre><code>python AutoStory.py</code></pre>
    </li>
    <li>
      <strong>Follow the interactive prompts:</strong>
      <ul>
        <li>Enter your hero’s name.</li>
        <li>Choose a hero archetype from the available options (Warrior, Mage, Rogue, Cleric).</li>
        <li>Select a starting location from the provided list.</li>
        <li>Continue the adventure by choosing to explore, interact with characters, or ask for guidance.</li>
      </ul>
    </li>
    <li>
      <strong>Enjoy your adventure:</strong>
      The narrative will be generated dynamically based on your choices and the context retrieved from the knowledge base.
    </li>
  </ol>
  
  <h2 id="code-overview">Code Overview</h2>
  <p>The project is organized into several key components:</p>
  <ul>
    <li><strong>Knowledge Base:</strong>  
      A simple dictionary that contains descriptions for locations, characters, and artifacts. This information is used to provide context during story generation.
    </li>
    <li><strong>Context Retrieval:</strong>
      The <code>retrieve_context</code> function fetches descriptive text from the knowledge base based on user choices (e.g., location, character, artifact).
    </li>
    <li><strong>Story Generation:</strong>
      The <code>generate_story</code> function sends a prompt (augmented with contextual information) to the OpenAI API and returns the generated narrative.
    </li>
    <li><strong>Interactive Functions:</strong>
      <ul>
        <li><code>create_character</code>: Prompts the user to input a hero’s name and select an archetype.</li>
        <li><code>choose_location</code>: Lets the user choose a starting location, ensuring valid input through normalization.</li>
        <li><code>interact_with_character</code>: Allows the user to pick a character from the knowledge base for an interaction.</li>
        <li><code>run_game</code>: The main function that runs the interactive narrative loop. Based on user choices, it generates new story events until the game is ended.</li>
      </ul>
    </li>
  </ul>
  
  <h2 id="algorithms">Algorithms and Technologies Used</h2>
  <p>
    AutoStory leverages the power of OpenAI’s language models (using the <code>gpt-3.5-turbo-instruct</code> engine by default) to create narrative text.
    The system uses a retrieval-augmented approach by incorporating contextual information from a predefined knowledge base into the prompts.
    This combination allows for dynamic, context-aware storytelling.
  </p>
  
  <h2>Additional Notes</h2>
  <p>
    The interactive narrative generator is designed to be easily expandable. You can add more archetypes, locations, characters, and artifacts to enrich the story.
    Feel free to modify the prompts or knowledge base to better suit your creative vision.
  </p>
  
</body>
</html>
