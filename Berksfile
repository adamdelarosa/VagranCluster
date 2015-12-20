source "https://supermarket.chef.io"



metadata
Dir['cookbooks/**'].each do |path|
  cookbook File.basename(path), path: path
end

#cookbook 'consul', path: 'cookbooks_more/'
#cookbook "consul"