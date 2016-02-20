require 'tilt'
require 'erb'
require 'asciidoctor'
 
guard 'shell' do
  watch(%r{^(.+)/(.+)\.adoc$}) { |m|
    Asciidoctor.render_file m[0], 
        :in_place => true,
        :safe => :unsafe,
        :backend => 'html5'
    n m[0], "Rebuilt"
  }
end 