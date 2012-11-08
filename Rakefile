def quakelive_baseq3
  File.expand_path("~/Library/Application\ Support/QuakeLive/quakelive/home/baseq3")
end

task :push do
  files = Dir.glob("*.cfg")
  files.each do |file|
    cp file, File.join(quakelive_baseq3, file)
  end
end

task :pull do
  exclude = ["qzconfig.cfg", "repconfig.cfg"]
  files = Dir.glob(File.join(quakelive_baseq3, "*.cfg"))
  files = files.reject {|f| exclude.include?(File.basename(f))}
  files.each do |file|
    cp file, File.basename(file)
  end
end
