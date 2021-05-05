# uptimerobot-parking

Parking any domain to Uptimerobot Status Page without PRO Plan.

## Get Status Page ID

Uptimerobot status page ID can found on your Uptimerobot status page url: `https://stats.uptimerobot.com/<status_page_id>`

## Using Docker

### Build your image:

```bash
git clone https://github.com/dangdungcntt/uptimerobot-parking.git
cd uptimerobot-parking
docker build -t uptimerobot-parking .
docker run -d \
    -e UPTIMEROBOT_DASHBOARD_ID=<status_page_id> \
    -p 8080:80 \
    uptimerobot-parking
```

### Use my image:

```bash
docker run -d \
    -e UPTIMEROBOT_DASHBOARD_ID=<status_page_id> \
    -p 8080:80 \
    dangdungcntt/uptimerobot-parking
```

Your status page can access via: `http://localhost:8080`

## Using native nginx installed on your system

Copy contents of `templates/default.conf.template` file and replace `${UPTIMEROBOT_DASHBOARD_ID}` with your `<status_page_id>`
