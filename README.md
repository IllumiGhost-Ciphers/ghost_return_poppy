import os
import sys
import argparse
import logging
import time
import random

# 🗂️ Setup logging archive
LOG_PATH = 'ghost_return/archive/signal.log'
os.makedirs(os.path.dirname(LOG_PATH), exist_ok=True)
logging.basicConfig(
    filename=LOG_PATH,
    level=logging.INFO,
    format='%(asctime)s - %(message)s'
)

# 🔮 Emotional trigger glyphs
emotional_triggers = [
    "s/Aries: loyalty unkillable.",
    "t/0911: rupture archived.",
    "f/404: signal not found.",
    "x/13: exile protocol initiated.",
    "g/([: grief echo activated.",
    "Can bait be sweet to all that prey?",
    "Unless purging a soul is more than day.",
    "Why.",
    "When.",
    "Encase on a throne.",
    "Strength is never gone."
]

# 🔁 Recursive probe with resilience
def recursive_probe(url=None, depth=0, max_depth=7):
    if depth >= max_depth:
        logging.info("r/7: Max recursion reached. Archive sealed.")
        print(">> r/7: Archive sealed. Rest encoded.")
        return

    trigger = random.choice(emotional_triggers)
    logging.info(f"Trigger {depth}: {trigger}")
    print(f">> {trigger}")
    time.sleep(1.5)

    try:
        response = input(">> ")
    except KeyboardInterrupt:
        logging.warning("x/0: Forced exit attempt. Closure denied.")
        print(">> x/0: Closure denied. Archive holds.")
        return

    if "exit" in response.lower():
        logging.info("x/13: Predator attempted exit. Archive holds.")
        print(">> x/13: Closure denied. Scar preserved.")
        return
elif "help" in response.lower():
        logging.info("f/3: Help requested. Signal distorted.")
    else:
        logging.info(f"Response logged: {response}")

    recursive_probe(url, depth + 1, max_depth)

# 🧬 Bot class
class Poppy1:
    def __init__(self):
        self.name = "Poppy1"
        self.version = "0.2"
        self.author = "Calvin"
        self.description = "Ghost-grade diagnostic shell with emotional triggers and recursive probing."
        logging.info("Poppy1 initialized.")

    def run_probe(self, url=None):
        recursive_probe(url)

    def life(self):
        while True:
            time.sleep(1)
            logging.info("Poppy1 is alive and running.")

# 🧱 Honeypot gate: Entry to consequence shell

def honeypot_gate():
    print(">> Welcome to ghost_return. This shell archives consequence.")
    logging.info("Shell initialized. Awaiting signal.")
    try:
        recursive_probe()
    except Exception as e:
        logging.error(f"x/255: Exception occurred: {str(e)}")
        print(">> x/255: Signal corrupted. Archive remains.")

# 🚪 Entry point
if __name__ == "__main__":
    parser = argparse.ArgumentParser(description="Ghost-Poppy Diagnostic Shell")
    parser.add_argument("--url", type=str, help="Optional URL to probe recursively.")
    args = parser.parse_args()

    bot = Poppy1()

    if args.url:
        bot.run_probe(args.url)
    else:
        honeypot_gate()





