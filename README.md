Repo To automatically install the ELK stack with ansible

# Requirments
The servers below has to be configured in the inventory file
* 3 elasticsearch servers
* 1 Kibana server
* 1 fleet server
* 1 logstash server

# Execute playbook
```bash
ansible-playbook -i inventory/hosts.ini site.yml -k --limit groepnaam --tags all
```

* In de host.ini zet je de servers neer waar je mee wilt communiceren.
* Met de groepnaam geef je aan tegen welke groep je de play wilt aftrappen.
* Met de tags (deze vind je terug in de site.yml) geef je aan welke rollen je wilt aftrappen.
* -k hiermee geef je de wachtwoord van jou user op om in te loggen op de remote server
* -K (optioneel) als je bij het root worden een wachtwoor moet opgeven, voeg je deze item toe
