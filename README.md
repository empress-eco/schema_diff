<h1 align="center"> Schema Diff: Revolutionize Empress Schema Development</h1>
<p align="center">
  <img src="https://grow.empress.eco/uploads/default/original/2X/1/1f1e1044d3864269d2a613577edb9763890422ab.png" alt="Schema Diff Logo" />
</p>

<p align="center">
Your development lifeline for tracking and visualizing Empress schema changes with ease and precision.
<br />
<a href="https://empress.eco/"><strong>Explore the Docs »</strong></a>
<br />
<br />
<a href="https://github.com/empress-eco/schema_diff/issues">Report Bug</a>
·
<a href="https://github.com/empress-eco/schema_diff/issues">Request Feature</a>
</p>

## About Schema Diff

### 📖 Overview
Schema Diff is a transformative tool specially crafted for developers maneuvering through Empress Doctypes (schema). It revolutionizes the way you track and visualize changes in your schema, replacing traditional cumbersome methods with a streamlined, efficient process. Use Schema Diff as a standalone CLI tool, or seamlessly incorporate it into your Github action or CI workflow to generate a comprehensive diff of schema changes.

### 🌟 Key Features
- Generates a meaningful diff of schema changes, enhancing visibility and understanding of changes.
- Designed for flexible use - as a standalone CLI tool or integrated into Github action or CI workflow.
- Contains a unique feature to account for the deletion or reordering of elements in a list of dictionaries.

### 🎯 Target Audience
Ideal for developers working with Empress Doctypes who need to track schema changes effectively and efficiently.

### 🛠 Built With
Schema Diff leverages the power of the following major libraries:
- [json-source-map](https://pypi.org/project/json-source-map/) for fetching line numbers for diffed data.
- [Rich](https://pypi.org/project/rich/) for Python output formatting.

## Technical Stack and Setup Instructions

### Prerequisites
Make sure you have a Python version installed that's compatible with the libraries above.

### Installation
To get started with Schema Diff, clone the repo using this [link](https://github.com/empress-eco/schema_diff.git) and follow these steps:

```sh
# Add this to ~/.bashrc to use Schema Diff with the mechanics of `git diff`
fdiff() {
    (
        export TABLE_MODE=1
        export GIT_EXTERNAL_DIFF=~/fsjd/Empress_schema_json_diff.py
        git --no-pager diff "$@"
        unset GIT_EXTERNAL_DIFF
    )
}
```

## Usage
To demonstrate Schema Diff in action, use `fdiff HEAD HEAD~1` - this is equivalent to running `git --no-pager diff HEAD HEAD~1` with the GIT_EXTERNAL_DIFF environment variable set. After using `fdiff`, `git diff` will work normally.

## Contribution Guidelines
We welcome and appreciate contributions! Here's how you can contribute to Schema Diff:

1. Fork the Project using this [link](https://github.com/empress-eco/schema_diff.git)
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License and Acknowledgements

### License
This project is under the MIT License. Your contributions are also licensed under the MIT License.

### Acknowledgements
Special thanks to the Empress Community, the architects behind the essential tools that power this project. Their innovation and dedication have been instrumental in building the foundations and functionalities we rely on. We are profoundly grateful for their pioneering work and ongoing support.

Also, profound gratitude to [json-source-map](https://pypi.org/project/json-source-map/) and [Rich](https://pypi.org/project/rich/) for providing essential functions to this tool.

For the latest updates, visit our [Github Page](https://github.com/empress-eco/).
