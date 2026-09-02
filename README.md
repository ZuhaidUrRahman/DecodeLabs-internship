def run_chatbot():
  # 1. Knowledge Base: Dictionary with 5+ intents (O(1) Direct Access)
  responses = {
      "hello": "Hi there! Welcome to DecodeLabs. How can I help you today?",
      "how are you": (
          "I am operating at peak deterministic efficiency, ready for your"
          " commands."
      ),
      "what is your name": (
          "I am your Project 1 Rule-Based AI Guardrail Chatbot."
      ),
      "help": (
          "I can respond to greetings, project info, and exit commands. Try"
          " asking about 'ai' or 'skills'."
      ),
      "ai": (
          "Artificial Intelligence starts with deterministic control flow"
          " before venturing into probabilistic models."
      ),
      "skills": (
          "Key skills for Project 1 include: Control flow, decision-making"
          " logic, and dictionary lookups."
      ),
  }

  print("=" * 60)
  print("DECODELABS AI - RULE-BASED CHATBOT INITIALIZED")
  print("Type 'exit' or 'quit' to terminate the session.")
  print("=" * 60)

  # 2. The Heartbeat: Continuous 'while' Infinite Cycle
  while True:
    # Capture raw feed from user
    raw_input_str = input("\nYou: ")

    # 3. Phase 1: Input & Sanitization (Normalization)
    clean_input = raw_input_str.lower().strip()

    # 4. Exit Strategy: Clean break command
    if clean_input in ["exit", "quit"]:
      print(
          "Bot: Terminating session. Goodbye! Keep building the foundation."
      )
      break

    # Handle empty input edge case gracefully
    if not clean_input:
      print("Bot: Please enter a valid command or question.")
      continue

    # 5. Industrial Implementation: The .get() Method for Lookup + Fallback
    reply = responses.get(clean_input, "I do not understand.")

    # Output generation
    print(f"Bot: {reply}")


if __name__ == "__main__":
  run_chatbot()
