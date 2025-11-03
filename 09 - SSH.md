

https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent

**1** - check for existing keys

`ls -al ~/.ssh`


**2 - generate a key**

`ssh-keygen -t ed25519 -C "monet.fort@greatminds.org"`

**3** When you're prompted to "Enter a file in which to save the key", you can press **Enter** to accept the default file location.


**3 - Add SSH key to ssh-agent**

`eval "$(ssh-agent -s)"`

`open ~/.ssh/config`

if doesn't exist

`touch ~/.ssh/config`

...etc

Copy key to clipboard

```
ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAILHPJMf5HtJf0euTOQlGZBUg4VoghvmLl5EspkSF8W4h monet.fort@greatminds.org
```


## Create your keys

https://github.com/settings/keys


**Adding a new key**

https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account


**Authenticate with SSO**

https://docs.github.com/en/enterprise-cloud@latest/authentication/authenticating-with-saml-single-sign-on/authorizing-an-ssh-key-for-use-with-saml-single-sign-on


**Signed commits**

https://docs.github.com/en/authentication/managing-commit-signature-verification/about-commit-signature-verification