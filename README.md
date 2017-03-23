<!-- Please don't remove this: Grab your social icons from https://github.com/carlsednaoui/gitsocial -->

<!-- display the social media buttons in your README -->

By Tim Hopper:
[tdhopper.com](http://www.tdhopper.com)

[![alt text][1.1]][1]
[![alt text][6.1]][6]


<!-- links to social media icons -->
<!-- no need to change these -->

<!-- icons with padding -->

[1.1]: http://i.imgur.com/tXSoThF.png (twitter icon with padding)
[2.1]: http://i.imgur.com/P3YfQoD.png (facebook icon with padding)
[3.1]: http://i.imgur.com/yCsTjba.png (google plus icon with padding)
[4.1]: http://i.imgur.com/YckIOms.png (tumblr icon with padding)
[5.1]: http://i.imgur.com/1AGmwO3.png (dribbble icon with padding)
[6.1]: http://i.imgur.com/0o48UoR.png (github icon with padding)

<!-- icons without padding -->

[1.2]: http://i.imgur.com/wWzX9uB.png (twitter icon without padding)
[2.2]: http://i.imgur.com/fep1WsG.png (facebook icon without padding)
[3.2]: http://i.imgur.com/VlgBKQ9.png (google plus icon without padding)
[4.2]: http://i.imgur.com/jDRp47c.png (tumblr icon without padding)
[5.2]: http://i.imgur.com/Vvy3Kru.png (dribbble icon without padding)
[6.2]: http://i.imgur.com/9I6NRUm.png (github icon without padding)


<!-- links to your social media accounts -->
<!-- update these accordingly -->

[1]: http://www.twitter.com/tdhopper
[6]: http://www.github.com/tdhopper

<!-- Please don't remove this: Grab your social icons from https://github.com/carlsednaoui/gitsocial -->


[Automating Python with Ansible](Automating%20Python%20with%20Ansible.ipynb) is an interactive tutorial about how to use the [Ansbile](https://www.ansible.com/) configuration management tool to run a long-running Python process on a remote machine in a repeatable manner. It's particularly oriented towards data scientists.


## Install Instructions

### [Install Ansible](http://docs.ansible.com/ansible/intro_installation.html)

* `$ brew install ansible` on a Mac.
* `$ sudo apt-get install ansible` on a Debian/Ubuntu system.

### Setup Jupyter Environment

* [Install Conda](https://conda.io/docs/installation.html)
* `$ conda env update` to create Conda environment from `environment.yml`.
* `$ source activate automating_python` (in Bash).
* `$ python -m bash_kernel.install` to install Jupyter bash kernel.


### Launch a Virtual Private Server

I used [DigitalOcean](https://www.digitalocean.com/). They have a nice UI and [clear instructions](https://www.digitalocean.com/community/tutorials/how-to-create-your-first-digitalocean-droplet-virtual-server). You'll want to [add an SSH key so you can ssh without a password](https://www.digitalocean.com/community/tutorials/how-to-set-up-ssh-keys--2).

### Setup `~/.ssh/config`

To make it easy to SSH to the box, add something like this to your `~/.ssh/config`:

```
Host digitalocean
  HostName VPS.IP.ADDR.ESS
  User root
  Port 22
  IdentityFile "/Users/USER/.ssh/id_rsa"
  ForwardAgent yes
```


### Launch Notebook

* `$ jupyter-notebook` to launch a local Jupyter notebook server.
* Open the `Automating Python with Ansible.ipynb` notebook.