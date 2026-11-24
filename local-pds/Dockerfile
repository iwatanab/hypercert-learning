# Local PDS image. Dependencies are installed on the host first (pnpm install in ./service),
# because this session's network cannot reach the official ghcr.io image.
FROM node:22-trixie-slim
WORKDIR /app
COPY service/ ./
EXPOSE 2583
ENV NODE_ENV=production
ENV UV_USE_IO_URING=0
CMD ["node", "--enable-source-maps", "index.ts"]
