# Monitor CI pipeline metrics with Tinybird
This repo includes Tinybird resources - a datasource file and nine (9) pipe files - to calculate some typical CI pipeline metrics based on data created by the [pytest-tinybird](https://github.com/tinybirdco/pytest-tinybird) plugin. You can use these as examples in your CI analytics development.

## How to use these files
These files are meant to be used in conjunction with the `pytest-tinybird` plugin. For more information, please read [this](link to blog post)

Follow these steps to make use of these files:
1. Install the [pytest-tinybird plugin](https://pypi.org/project/pytest-tinybird/) in your pytest environment using the Python package installer [pip](https://pip.pypa.io/en/stable/). 
2. Create a [free Tinybird account](https://www.tinybird.co/signup?referrer=github) and set up a Workspace.
3. Clone this repo and use the [Tinybird CLI](https://www.tinybird.co/docs/quick-start-cli.html) to push the files to your Workspace.
4. Set three environment variables in your pytest environment:
   
  - ``TINYBIRD_URL``: For example ``https://api.tinybird.co`` or ``https://api.us-east.tinybird.co`` depending on your Workspace region.
  - ``TINYBIRD_DATASOURCE``: The name of your Data Source in Tinybird, e.g. ``test_reports`` in this repo.
  - ``TINYBIRD_TOKEN``: A Tinybird [Auth Token](https://www.tinybird.co/docs/concepts/auth-tokens.html) with DATASOURCE:WRITE permissions.

5. Run your instance of pytest with the `--report-to-tinybird` option.
6. Use your Tinybird APIs as you'd like!
