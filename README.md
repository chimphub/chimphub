# Chimphub

This Github app enables integration between Github repositories and Mailchimp. This way, you can enable source control of your precious newsletter templates.

Additionally, you can add whatever preprocessors and other magic you want that can build your project.

### Installation

To get started, set up an account on [chimphub.io](https://chimphub.io). Then, you install the app to your Github account.

Now, you can add a `.chimp.json` file to your project with the proper configuration, and you're good to go!

### Open source

This service is open source, but we do offer the backend as a paid subscription.

### Example config

```
{
    "template": {
        "name": "Test template",
        "source": "dist/index.html",
        "prepublish": [
            { "action": "npm install" },
            { "action": "npm run build" },
        ],
        "preprocessors": [
            {
                "type": "sass",
                "source": "src/styles/main.scss",
                "inline": true,
            }
        ]
    }
}
```
