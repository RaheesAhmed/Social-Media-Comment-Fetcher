# Social Media Comment Fetcher

This Node.js script fetches comments or tweets related to a specific topic ("G20") from Twitter, YouTube, and Google News.

## Table of Contents

- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [Notes](#notes)
- [License](#license)

## Installation

1. Clone this repository:
    ```bash
    git clone https://github.com/your-repo/social-media-comment-fetcher.git
    ```

2. Navigate to the project directory:
    ```bash
    cd social-media-comment-fetcher
    ```

3. Install the required npm packages:
    ```bash
    npm install twit googleapis axios cheerio
    ```

## Configuration

1. Open the `index.js` file and replace the placeholders for Twitter and YouTube API keys and tokens.

    ```javascript
    const T = new Twit({
      consumer_key: 'YOUR_CONSUMER_KEY',
      consumer_secret: 'YOUR_CONSUMER_SECRET',
      access_token: 'YOUR_ACCESS_TOKEN',
      access_token_secret: 'YOUR_ACCESS_TOKEN_SECRET',
    });

    const youtube = google.youtube({
      version: 'v3',
      auth: 'YOUR_YOUTUBE_API_KEY',
    });
    ```

2. For YouTube, you'll need to specify a `VIDEO_ID` to fetch comments from.

    ```javascript
    const youtubeComments = await fetchYoutubeComments('VIDEO_ID'); // Replace 'VIDEO_ID' with the actual video ID
    ```

## Usage

1. Run the script:

    ```bash
    node index.js
    ```

2. Check the console for the fetched comments from Twitter, YouTube, and Google News.

## Notes

- The Google News part is a placeholder; you may need to adjust the scraping logic as per your needs.
- Make sure to abide by the terms of service of each platform when using this script.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
