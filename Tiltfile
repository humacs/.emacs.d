# -*- mode: python; -*-
k8s_yaml(kustomize('.'))
# Lists of ports are broken. When having [P1, P2, P3], P2 and P3 get forwarded
# to P1. Unless in the N:N format.
# k8s_resource('session', port_forwards=[
#     '2200:2200',  # ssh
#     '4001:4001']) # http
# k8s_resource('master', port_forwards=[
#     '4000:4000',  # http
#     '9100:9100']) # metrics port
# k8s_resource('postgres', port_forwards=[5432])

# docker_build('tmate/tmate-ssh-server',
#              '../../../../tmate-ssh-server',
#              dockerfile='../../../../tmate-ssh-server/Dockerfile',
#              # dockerfile='../../../../tmate-ssh-server/Dockerfile.dev',
#              live_update=[
#                  fall_back_on(['../../../../tmate-ssh-server/Makefile.am']),
#                  sync('../../../../tmate-ssh-server',
#                       '/src/tmate-ssh-server'),
#                  run('make -j "$(nproc)"'),
#                  restart_container()]
# )

# docker_build('tmate/tmate-websocket',
#              '../../../../tmate-websocket',
#              dockerfile='../../../../tmate-websocket/Dockerfile',
#              # dockerfile='../../../../tmate-websocket/Dockerfile.dev',
#              live_update=[
#                  fall_back_on(['../../../../tmate-websocket/config',
#                                '../../../../tmate-websocket/mix.exs',
#                                '../../../../tmate-websocket/mix.lock']),
#                  sync('../../../../tmate-websocket',
#                       '/src/tmate-websocket'),
#                  run('echo recompile > console')]
# )

# docker_build('tmate/tmate-master', '../../../../tmate-master',
#              dockerfile='../../../../tmate-websocket/Dockerfile',
#              # dockerfile='../../../../tmate-master/Dockerfile.dev',
#              live_update=[
#                  fall_back_on(
#                      ['../../../../tmate-master/config',
#                       '../../../../tmate-master/assets/package.json',
#                       '../../../../tmate-master/assets/package-lock.json',
#                       '../../../../tmate-master/mix.exs',
#                       '../../../../tmate-master/mix.lock']),
#                  sync('../../../../tmate-master', '/src/tmate-master'),
#                  run('echo recompile > console')]
# )
allow_k8s_contexts('in-cluster')
