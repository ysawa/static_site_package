guard 'sass', input: 'assets/css'
guard 'coffeescript', input: 'assets/js'

guard 'haml', input: 'views', output: 'views', haml_options: { ugly: true } do
  watch(%r{^.+(\.haml)$})
end

guard 'shell' do
  watch %r{^views/(.*)\.php\.html$} do |m|
    `ls views/#{m[1]}.php.html && mv views/#{m[1]}.php.html #{m[1]}.php`
    n "#{m[0]} was changed to #{m[1]}.php", 'mv', :success
    "#{m[0]} was changed to #{m[1]}.php"
  end
end
