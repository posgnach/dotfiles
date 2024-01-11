# prefix should be CTRL+a because who the hell can press CTRL+b comfortably with one hand?
unbind C-b
set -g prefix C-a
bind C-a send-prefix

# better color support
set -g default-terminal "screen-256color"

# vim key bindings
set-window-option -g mode-keys vi

# pane movement shortcuts
bind h select-pane -L
bind j select-pane -D
bind k select-pane -U
bind l select-pane -R

# Notify on status bar when window has activity
setw -g monitor-activity off
set -g visual-activity off

# Rather than constraining window size to the maximum size of any client
# connected to the *session*, constrain window size to the maximum size of any
# client connected to *that window*. Much more reasonable.
setw -g aggressive-resize on

# make delay shorter
set -sg escape-time 0

# make window/pane index start with 1
set -g base-index 1
setw -g pane-base-index 1

# automatically renumber tmux windows
set -g renumber-windows on

set -g terminal-overrides 'xterm*:smcup@:rmcup@'
set-window-option -g xterm-keys on

# reload config file
bind r source-file ~/.config/tmux \; display "Config Reloaded!"

# synchronize all panes in a window
bind y setw synchronize-panes

bind -r C-h select-window -t :-
bind -r C-l select-window -t :+

# Resize pane shortcuts
bind -r H resize-pane -L 10
bind -r J resize-pane -D 10
bind -r K resize-pane -U 10
bind -r L resize-pane -R 10

bind | split-window -h -c "#{pane_current_path}"
bind - split-window -v -c "#{pane_current_path}"
unbind '"'
unbind %

