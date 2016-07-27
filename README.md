# Template to generate html formatted email

This project allows the automatic generation of html formatted emails using [pandoc](http://pandoc.org).

To generate a new html email, write your content in markdown (see: `example.md`) and run the following code in your terminal:

```
$ pandoc example.md --template email_template.html -o example.html
```

# Send

You need to send the email using a client that allows proper embedding of html.

You can use [Thunderbird](https://www.mozilla.org/en-GB/thunderbird/) using the `Insert>HTML` option when composing the message, but be sure to **always** include the following image attribute in your markdown file:

```
[image name](http://www.example.com/image.jpg){moz-do-not-send="true"}
```

This prevents Thunderbird from attaching the files instead of including them as linked references. Thus the email is far smaller and is less likely to be blocked by spam filters.

Also, while the template will automatically limit the max-width of inline images to 460px, it is best if the source images are resized to a max width of 460~490 pixels to ensure broad email client compatibility.


# Acknowledgements

The template was adapted from [MailChimp templates](https://github.com/mailchimp/email-blueprints).


# License

This code is available under a [Creative Commons Attribution-ShareAlike 3.0 Unported License](https://creativecommons.org/licenses/by-sa/3.0/).
