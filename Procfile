web: bundle exec unicorn_rails -c config/unicorn.rb -p $PORT
sidekiq: bundle exec sidekiq
slow_worker: bundle exec sidekiq -q socket_webfinger -q photos -q http_service -q dispatch -q receive_local -q mail -q receive -q receive_salmon -q http -q delete_account 
priority_worker: bundle exec sidekiq -q socket_webfinger -q photos -q http_service -q dispatch -q mail -q delete_account 
super_slow_worker: bundle exec sidekiq -q http -q receive_salmon