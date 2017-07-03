https://www.flickr.com/photos/78144310@N04/33645034336/
https://www.flickr.com/photos/90692748@N04/23835028019/


Total rubygems: 134421
Top rubygems (over 1000 dependent repos): 1098

TODO - script to download and check license of latest version of each rubygem with licensee


# bus factor csv - https://gist.github.com/andrew/4659f62704a0d719cd7d370de75d1539

top = Project.platform('rubygems').not_removed.where('dependent_repos_count > 999').joins(:registry_permissions).select('projects.*, count(registry_permissions.id) AS rp_count').group('projects.id').sort_by{|p| [p.rp_count, -p.dependent_repos_count]}
top.each {|p| puts "#{p.name},#{p.rp_count},#{p.dependent_repos_count}" };nil

38% of top rubygems only have one owner

1337 unique owners of



p = Licensee.project '/Users/andrew/code/file_browser/data/split/0.1.0', detect_readme: true, detect_packages: true
