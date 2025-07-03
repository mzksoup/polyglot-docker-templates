FROM node:20

RUN apt-get update && apt-get install -y curl unzip tar

# Install Supabase CLI
RUN ARCH=$(uname -m) && \
    if [ "$ARCH" = "x86_64" ]; then \
        SUPABASE_ARCH="amd64"; \
    elif [ "$ARCH" = "aarch64" ]; then \
        SUPABASE_ARCH="arm64"; \
    else \
        SUPABASE_ARCH="amd64"; \
    fi && \
    curl -sL "https://github.com/supabase/cli/releases/latest/download/supabase_linux_$SUPABASE_ARCH.tar.gz" \
    -o /tmp/supabase.tar.gz && \
    tar -xzf /tmp/supabase.tar.gz -C /tmp && \
    mv /tmp/supabase /usr/local/bin/supabase && \
    chmod +x /usr/local/bin/supabase && \
    rm /tmp/supabase.tar.gz

WORKDIR /workspace
