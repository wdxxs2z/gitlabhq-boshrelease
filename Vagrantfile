Vagrant::Config.run do |config|
  config.vm.box = "bosh-solo-0.6.4"
  config.vm.box_url = "http://files.vagrantup.com/lucid64.box"

  # config.vm.forward_port 80,   5001
  config.vm.network :hostonly, "33.33.33.30"

  config.vm.provision :shell, :path => "scripts/vagrant-setup.sh"

  if local_bosh_src = ENV['BOSH_SRC']
    config.vm.share_folder "bosh-src", "/bosh", local_bosh_src
  end
end
