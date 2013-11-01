


task :default do

  File.open('README.md', 'w') do |out|

    out.puts "# My Pagists"
    out.puts
    out.puts "This is a collection of my [Pagists](http://www.pagist.info/)."
    out.puts

    File.read('.gitmodules').scan(/path = (\S+)\s+url = (\S+)/).sort_by(&:first).reverse.each do |path, url|
      out.puts "* [#{path}](http://www.pagist.info/#{url.scan(/(\d+)\.git/).first.first})"
    end

  end

end
