python -m venv .venv
source .venv/bin/activate
python -m pip install ansible ansible-rulebook ansible-runner psycopg
ansible-galaxy collection install ansible.eda
ansible-rulebook --rulebook demo_rule.yml -i inventory.yml --verbose


# On another terminal and on same directory run this and test the Rulebook


curl -X POST -H "Content-Type: application/json" -d @42.json 127.0.0.1:5000/endpoint