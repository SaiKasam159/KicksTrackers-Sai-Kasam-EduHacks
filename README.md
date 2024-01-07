## Inspiration

The idea for this code stemmed from a need to stay informed about discounts and secure limited-edition releases. The goal was to create a web scraping tool to monitor Nike and Snkrs APIs efficiently, addressing the competitive nature of the sneaker market. The code aims to provide timely information, aiding in making well-informed purchasing decisions within the sneaker community. I also use this to help me find sneakers to resell for a profit.

## What it does

The code essentially utilizes GET requests to retrieve JSON responses from the APIs that Nike and Snkrs use to refresh their websites. The code then iterates through each shoe, filters them according to certain conditions like whether they are discounted or not, whether they are bestsellers or not, checks for specified wanted or unwanted phrases, etc. After that, it sends me a Discord message with details such as the price, an image, whether the shoe is discounted, whether it's a bestseller, the colorway, and the original full price of the shoe. This information helps me decide whether the shoe is worth buying in order to resell for a profit.

## How we built it

I created this script using Python for its versatility and efficiency. The script extracts real-time product information from Nike and Snkrs APIs by scraping their websites. I utilized Python's _requests_ and _json_ libraries and integrated the _FreeProxy_ library for web scraping anonymity. Discord webhooks are employed to send the information to a custom Discord server I created. The primary purpose of the code is to compare the newly scraped shoe data with existing data to quickly identify any availability changes. Additionally, there is a filtering mechanism in place that refines the results based on criteria such as discounts, bestseller status, and price ranges. I used Visual Studio Code and GitHub for version control and collaboration. I then set it to run every time my computer starts up using Windows Task Manager.

## Challenges we ran into

To address rate limiting challenges posed by Nike and Snkrs APIs, I implemented controlled pauses between consecutive requests, I ensured compliance with the platforms' rate limits, preventing disruptions due to excessive requests. This approach optimized the scraping process and also maintained the script's efficiency.

Another issue  faced was being blocked from accessing the Nike and Snkrs APIs due to anti web scraping measures. To overcome this issue, I utilized a proxy server from the Python library called "Free Proxy" and incorporated headers that enabled anonymous browsing. This approach allowed me to work around the anti-webscraping measures, ensuring access to the APIs without being blocked.

## Accomplishments that we're proud of

The project runs every single day, and every day I get updates and insights without fail. Also, I ran the code on my friend's computer which ensures that the code is reproducible.

## What we learned

I learnt how to effectively web scrape sites and utilize discord webhooks to send messages to myself. I also learnt how to make scripts run automatically on servers and Windows machines. I also need to make it send the URL for the shoe in the discord webhook, as well as availability of different shoe sizes..

## What's next for KicksTrackers

I want to make the code run on a server on Linode or AWS so that it is completely automated. I can also expand this code to scrape StockX and Footaslyum or other sites.
