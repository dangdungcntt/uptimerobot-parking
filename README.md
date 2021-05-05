# uptimerobot-parking

Parking any domain to Uptimerobot Status Page without PRO Plan.

# Get Status Page ID

Uptimerobot status page ID can found on your Uptimerobot status page url: `https://stats.uptimerobot.com/<status_page_id>`

# Using Docker

```bash
git clone https://github.com/dangdungcntt/uptimerobot-parking.git
cd uptimerobot-parking
docker build -t uptimerobot-parking .
docker run -d \
    -e UPTIMEROBOT_DASHBOARD_ID=<status_page_id> \
    uptimerobot-parking
```

# Using native nginx installed on your system

Copy contents of `templates/default.conf.template` file and replace `${UPTIMEROBOT_DASHBOARD_ID}` with your `<status_page_id>`
