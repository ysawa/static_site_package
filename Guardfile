guard 'sass', input: 'assets/css'
guard 'coffeescript', input: 'assets/js'

guard 'haml', haml_options: { ugly: true } do
  watch %r{^views/.+(\.html\.haml)}
  watch %r{^views/.+(\.php\.haml)}
end

guard 'shell' do
  watch %r{^views/(.*)\.php\.html$} do |m|
    `mv views/#{m[1]}.php.html #{m[1]}.php`
  end
end
