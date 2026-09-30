# OpenWebUI Sandbox

Links:
 - https://openwebui.com/
   - https://github.com/open-webui/open-terminal
 - https://openrouter.ai/

Here is what I did:

- Create an account at https://openrouter.ai/
  - Load it with a little money (like $10) and get an API key
- Rename `.env.example` to `.env` and fill in you Openrouter API key
- Start it with `docker compose up`
- Make sure `open-terminal` can use Github CLI
  - `docker exec -it open-terminal bash` and `gh auth login`
  - Test it from outside Docker: `docker exec open-terminal sh -c 'echo "terminal works"; gh auth status'`
- In OpenWebUI, configure Terminal
  - `Settings` / `Integrations` / `Open Terminal`
  - User URL that is printed when container starts
  - Set Auth Bearer with value of `WEBUI_SECRET_KEY`
