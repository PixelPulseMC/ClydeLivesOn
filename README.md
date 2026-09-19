# Clyde (Clyde Lives On)
Clyde Dream is a Discord AI companion built to bring back the familiar, seamless interaction of Discord's original native Clyde bot. Powered by Gemini, Clyde auto-replies directly within assigned text channels without requiring rigid slash commands for every single interaction.Features
 * Channel Auto-Response: Automatically listens and responds to standard messages in assigned channels.
 * Gemini AI Integration: Utilizes Google's Gemini models for conversational text generation.
 * Lightweight & Portable: Designed to run in lightweight environments, including self-hosted mobile setups via Termux.
Quick Setup Guide
1. Prerequisites
 * Python 3.10+
 * A Discord Bot Token (via Discord Developer Portal)
 * A Gemini API Key (via Google AI Studio)
2. Installation
Clone the repository and install the required dependencies:
git clone https://github.com/PixelPulseMC/ClydeLivesOn.git
cd ClydeLivesOn
pip install -r requirements.txt

3. Environment Configuration
Create a .env file in the root directory and add your environment variables:
# Core API Keys
DISCORD_TOKEN=your_discord_bot_token_here
GEMINI_API_KEY=your_gemini_api_key_here

# Database Configuration
STATS_DB=stats.db
LOGS_DB=logs.db

# Dummy Variables (Bypasses unused legacy modules)
GROQ_API_TOKEN=unused
IMAGE_GEN_TOKEN=unused

> Security Note: Never commit your .env file or expose your actual API keys and tokens in public repositories. Keep .env added to your .gitignore.
> 
4. Setting Up Auto-Reply Channel
To bind Clyde to a specific channel:
 * Enable Developer Mode in your Discord settings.
 * Right-click / long-press your target channel and select Copy Channel ID.
 * Update the AUTO_CHANNEL_ID inside bot/events.py with your channel ID:
AUTO_CHANNEL_ID = 123456789012345678  # Replace with your copied channel ID

5. Running the Bot
Start the bot locally:
python main.py

Credits & License
 * Created and maintained by the PixelPulse team & Vadex Studios.
 * Built on top of the hikari and lightbulb Discord frameworks for Python.
