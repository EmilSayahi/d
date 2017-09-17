require 'html-proofer'

task :test do
  HTMLProofer.check_directories(
    ["./_site"], {
      :allow_hash_href => true,
      :parallel => {:in_processes => 4},
      :only_4xx => true,
      :url_ignore => ["/^(?:http(?:s)?:\/\/)?(?:[^\.]+\.)?drupal\.org(?:/.*)?$/",
                      "/^(?:http(?:s)?:\/\/)?(?:[^\.]+\.)?linkedin\.com(?:/.*)?$/",
                      "/^(?:http(?:s)?:\/\/)?(?:[^\.]+\.)?fldrupal\.camp(?:/.*)?$/"],
      :empty_alt_ignore => false,
      :verbose => true,
      :typhoeus => {
        :timeout => 3 }
    }).run
end