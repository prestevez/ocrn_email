---
filename: index.html
---

# Template to generate html formatted email

This project allows the automatic generation of [UCL Organised Crime Research Network](http://blogs.ucl.ac.uk/organised-crime/) html-formatted emails using [pandoc](http://pandoc.org).

To generate a new html email, write your content in markdown (see: `example.md`) and run the following code in your terminal:

```
$ pandoc example.md --template email_template.html -o filename.html
```

**Note that the use of this template is restricted to [UCL OCRN](http://blogs.ucl.ac.uk/organised-crime/) members of the steering committee for official email communications**.

You may adapt this template for your purposes by making sure it does not mention or link to UCL and UCL OCRN content.

## Archive

To be sure that the generated html-email is stored in the archive, so that recipients may see it in a browser and not their email client, save the output file into the `archive/` directory and give it a `filename` that coincides with the one that needs to be present in the YAML metadata at the beginning of the markdown file.

## Example

View an example [here](http://www.prestevez.com/ocrn_email/archive/JulySeminar.html).

# Send

You need to send the email using a client that allows proper embedding of html.

You can use [Thunderbird](https://www.mozilla.org/en-GB/thunderbird/) using the `Insert>HTML` option when composing the message, but be sure to **always** include the following image attribute (the bit between the curly brackets) in your markdown file:

```
[image name](http://www.example.com/image.jpg){moz-do-not-send="true"}
```

This prevents Thunderbird from attaching the files instead of including them as linked references. Thus the email is far smaller and is less likely to be blocked by spam filters.

Also, while the template will automatically limit the max-width of inline images to 460px, it is best if the source images are resized to a max width of 460~490 pixels to ensure broad email client compatibility.


# Acknowledgements

The template was adapted from [MailChimp templates](https://github.com/mailchimp/email-blueprints).


# License

This code is available under a [Creative Commons Attribution-ShareAlike 3.0 Unported License](https://creativecommons.org/licenses/by-sa/3.0/).
