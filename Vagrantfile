ENV['VAGRANT_DEFAULT_PROVIDER'] = 'docker'

Vagrant.configure("2") do |config|
  config.vm.define 'app', primary: true do |machine|
    machine.vm.provider "docker" do |d|
      d.build_dir = "."
      d.build_args = ["-t=app", "--rm=true"]
      d.has_ssh = true
      d.name = "app"
    end
    machine.ssh.insert_key = 'true'
  end
end
